<template>
  <div class="Counter">
    counter Value {{xCounter}} <br /><br />
    <button v-on:click="addMe" type="button">click + </button>
    <button v-on:click="xCounter++" type="button">click2 + </button>
    <h1>s: {{this.personName}}</h1>
    <button class="btnSetName" v-on:click="() => $emit('emit-setName', this.inpValue)">setName</button>
    <input type="text" v-on:keyup="getTextInput" v-model="inpValue" />
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
        xCounter: 0,
        inpValue: 'g'
      }
    },
    methods: {
      addMe(e) {
        console.log(e)
        this.xCounter++
      },
      getTextInput(e) {
        console.log('getTextInput', e)
        this.$emit('emit-setName', e.target.value)
      }
    }

}
</script>

<style>

</style>
