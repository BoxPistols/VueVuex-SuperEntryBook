# vuex-app-r291

## Explanation

This is a Vue learning repository

Use document:

- Books
    - Super introduction
    - Kaeru
    - Classroom
    - Cat
    - Nuxt Beginner
- Video
    - Udemy
    - Dott
    - You tube

## Menu

- router
- Props
- Vuex
    - store
- API
    - axios
    - json

---

## Do API Test use json

- create db.json
- $ npm install -g json-server or $ npm install --save-dev json-server
- $ npx json-server --watch db.json

 ### Create
$ curl --data-urlencode "name=Dummy api test" http://localhost:3000/todos/

### Update
$ curl -X PUT --data-urlencode "name=Update this" http://localhost:3000/todos/2

### Delete
$ curl -X DELETE http://localhost:3000/todos/3

---

## Docs

API Driven Application with Vue.js, JSON-Server and Axios:
https://www.youtube.com/watch?v=yNrqlxn0nc0

JSON Serverで作るダミーAPI
https://www.to-r.net/media/json-server/

---

## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn serve
```

### Compiles and minifies for production
```
yarn build
```

### Lints and fixes files
```
yarn lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
