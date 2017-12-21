<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <form-component id="example-form" :schema="schema"></form-component>
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
      msg: 'Welcome to Your Vue.js App',
      schema: {
        fields: [
          {
            type: 'text',
            id: 'text-field',
            label: 'Text field',
            description: 'This is a cool text field',
            visible: true,
            required: true,
            disabled: false,
            validators: [
              (value) => {
                const valid = value.indexOf('test') !== -1
                const message = valid ? '' : 'not valid value. Please include the word test'
                return {
                  valid: valid,
                  message: message
                }
              }
            ]
          }
        ]
      }
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
