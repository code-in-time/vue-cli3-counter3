<template>
  <div class="Counter">
    counter Value {{xCounter}} <br /><br />
    <button v-on:click="addMe" type="button">click + </button>
    <button v-on:click="xCounter++" type="button">click2 + </button>
    <h1>s: {{this.personName}}</h1>
    <button class="btnSetName" v-on:click="() => $emit('emit-setName', 'nnnnnnnnnn')">setName</button>
  </div>
</template>

<script>
export default {
    name: 'Counter',
    // props: ['personName'],
    props: {
      personName: String
    },
    data() {
      return {
        xCounter: 0
      }
    },
    methods: {
      addMe(e) {
        console.log(e)
        this.xCounter++
      }
    }

}
</script>

<style>

</style>
