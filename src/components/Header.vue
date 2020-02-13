<template>
  <header>
      <h1 v-on:click="changeTitle">{{ title }}</h1>
  </header>
</template>

<script>
export default {
  props: {
    title: {
      type: String
    }
  },
  data () {
    return {
    }
  },
  methods: {
    changeTitle() {
      //this.title = "Changed title..."
      this.$emit('changeTitle','event called changeTitle was emitted on clicking this title, and this is the next text!')
    } 
  }
}
</script>

<style scoped>
header{
    background: lightgreen;
    padding: 10px;
}
h1{
    color:#222;
    text-align: center;
}

</style>
