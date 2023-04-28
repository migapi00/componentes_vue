<template>
  <div> {{ text }}</div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      text: "Hola Luis"
    };
  },
beforeCreate(){
  console.log("beforeCreate", this.$data, this.$el);
},

created(){
  console.log("create", this.$data, this.$el);
},
mounted(){
  console.log("mounted", this.$data, this.$el);
},

}
</script>

<style>

</style>

