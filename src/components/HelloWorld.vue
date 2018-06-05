<template>
  <div>
    <helloworld-card></helloworld-card>
    <b-form-input v-model="fullName" type="text" placeHolder="Enter your name"></b-form-input>
    <b-button v-on:click="onEmit()">Emit Event</b-button>
  </div>
</template>

<script>
  import HelloWorldCard from './HelloWorldCard.vue'

  export default {
    name: 'HelloWorld',
    data() {
      return {
        fullName: ''
      }
    },
    components: {
      'helloworld-card': HelloWorldCard
    },
    methods: {
      onEmit() {
        this.$emit('GREET_EVENT', this.fullName);
      }
    }
  }

</script>

<style>
  h1,
  h2 {
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
