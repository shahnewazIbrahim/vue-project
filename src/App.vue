<template>
  <div>
    <Header :myName="name"
      :students="students"
      :firstName="fName"
      :lastName="lName"
      :age="myAge"
      @updateValue="fName = $event"
    />
    <p>{{ name }}</p>
    <Footer
      :lastName="lName"
    />
  </div>
</template>

<script>
import Header from "./Components/Header_footer/Header.vue"
import Footer from "./Components/Header_footer/Footer.vue"
  export default {
    data() {
      return {
        name: 'Himu',
        students: ["Saiful", "Himu", "Rashed", "Abid"],
        fName: 'John',
        lName: 'Doe',
        myAge: 21
      }
    },
    components : {
      Header,
      Footer
    }
  }
</script>

<style>
  div { 
    color: plum;
    font-family: 'Luxurious Roman', cursive;
  }
</style>