<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <form-component></form-component>
  </div>
</template>

<script>
import FormComponent from '@molgenis/molgenis-ui-form'

export default {
  name: 'HelloWorld',
  components: {
    FormComponent
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
