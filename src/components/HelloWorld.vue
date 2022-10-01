<template>
  <div class="box" @click="soma">
    <p>TESTANDO</p>
    <h1> {{anel}}</h1>
    <slot name="testes">
      <div>
        <h1>ddgdf</h1>
      </div>

    </slot>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  events: ['on-teste'],
  props: {
    anel: String
  },

  methods: {
    soma () {
      this.$emit("on-teste", {})
    },

    digaoi(){
      console.log("oláa");
    }
  }
}

</script>

<style scoped>
  .box {
    height: 300px;
    width: 300px;
    background-color: blue;
  }

  p {
    color: black !important; 
  }

</style>