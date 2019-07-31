# API with NOW

To have a lambda backend on `now`, you simply need to have an `api` folder at the root of the project.

The api routing is folder-based, so to have an endpoint at `/api/users/me` you would need a folder structure like this:

```
- api
  - users
    - me.js
```

You can use multiple languages together, so you could modify the folder structure to the following without any problems (as long as the language is supported):

```
- api
  - users
    - me.js
    - get.go
    - delete.rs
```

When you deploy the application, the backend will automatically be hosted for you as well in a (usually) a matter of seconds. It's that easy!