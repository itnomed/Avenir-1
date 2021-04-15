<template>
  <div class="container" @click="changeNameHandler">
    {{name}} {{surname}}
  </div>
</template>
<script>
  export default{
    props(){
     
    },
    data(){
      return {
        name: "John",
        surname: "kdsjfksdjf"
      }
    },
    methods: {
      changeNameHandler (){
        if (this.surname === "Black") {
           this.name = "Alice"
        }
      }
    },
    mounted() {
      console.log("before if " + this.surname)
       if(this.name === "John"){
         this.surname= "Black";
       }
       console.log("after " + this.surname);
    },
    created() {

    },
    destroyed() {

    }
  }
</script>
<style >
  .container {
    color: red;
    margin: 0 auto;
    width: 80%;
    font-size: 28px;
  }
</style>