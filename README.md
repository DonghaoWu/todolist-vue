# todolist-vue

1. install Vue Cli.

```bash
$ npm i --global vue-cli
```

2. create a vue 2 project

```bash
$ vue create client
$ cd client
$ npm run serve
```

3. add external library into Html file.

```html
<head>
  <meta charset="utf-8" />
  <meta http-equiv="X-UA-Compatible" content="IE=edge" />
  <meta name="viewport" content="width=device-width,initial-scale=1.0" />
  <link rel="icon" href="<%= BASE_URL %>favicon.ico" />
  <title><%= htmlWebpackPlugin.options.title %></title>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
  <link
    rel="stylesheet"
    type="text/css"
    href="https://cdnjs.cloudflare.com/ajax/libs/semantic-ui/2.2.7/semantic.min.css"
  />
  <script src="https://cdnjs.cloudflare.com/ajax/libs/semantic-ui/2.2.7/semantic.min.js"></script>
  <link
    rel="stylesheet"
    type="text/css"
    href="https://cdnjs.cloudflare.com/ajax/libs/sweetalert/1.1.3/sweetalert.min.css"
  />
  <script src="https://cdnjs.cloudflare.com/ajax/libs/sweetalert/1.1.3/sweetalert.min.js"></script>
</head>
```

4. create a component.

```vue
<template>
  <div>
    <ul>
      <li>Todo A</li>
      <li>Todo B</li>
      <li>Todo C</li>
    </ul>
  </div>
</template>

<script type="text/javascript">
export {};
</script>

<style></style>
```

5. create a vue file shorthand

```vscode
vue
```

6. importing components. :gem::gem::gem:

- App.vue

```js
import TodoList from './components/TodoList';
import Hello from './components/Hello';
```

7. adding component data

- set up variables and pass them down to component.

- accept data from parent component.

- Looping and rendering data

- add variable inside a tag

- add variable between tag

- v-show depends on variables

- passing looping variables to components.

8. editing todos.

- bind a click event listener

- bind a two ways data binding input field

- v-model to control the data state.

- 
