<template>
<div>
    <ul>
        <li v-for="todo in todos" :key="todo.id">
            <input type="text" v-model="todo.name" />
            <input type="button" value="編集/更新" @click="update(todo)" />
            <input type="button" value="削除" @click="remove(todo)" />
        </li>
    </ul>
    <input type="text" v-model="new_todo">
    <input type="button" value="追加" @click="create">
</div>
</template>

<script>
export default {
    data() {
        return {
            todos: [],
            new_todo: null
        }
    },
    created() {
        this.read()
    },
    methods: {

        // 一覧描画
        read() {
            fetch('http://localhost:3000/todos')
                .then(res => res.json())
                .then(res => this.todos = res)
        },

        // 新規追加
        create() {
            fetch('http://localhost:3000/todos', {
                    method: 'POST',
                    body: JSON.stringify({
                        name: this.new_todo
                    }),
                    headers: new Headers({
                        'Content-type': 'application/json'
                    })
                })
                .then(() => {
                    this.todos.push({
                        name: this.new_todo
                    })
                    this.new_todo = ''
                })
        },

        // 編集
        update(todo) {
            fetch(`http://localhost:3000/todos/${todo.id}`, {
                method: 'PUT',
                body: JSON.stringify({
                    name: todo.name
                }),
                headers: new Headers({
                    'Content-type': 'application/json'
                })
            })
        },

        // 削除
        remove(todo) {
            fetch(`http://localhost:3000/todos/${todo.id}`, {
                    method: 'DELETE'
                })
                .then(() => {
                    this.todos = this.todos.filter(item => item !== todo)
                })
        }
    }
}
</script>

<style lang="scss" scoped>

</style>
