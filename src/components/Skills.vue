<template>
  <div class="hello">
    <div class="holder">
      <ul>
        <li v-for="(data, index) in skills" :key='index'>{{ index}}. {{data.skill}}</li>
      </ul>

     

      <div v-bind:class="alertObject"></div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'Skills',
  data(){
    return {
      skills: [
        {"skill":"Vue.js" },
        {"skill":"Baseball" },
      ],
      showAlert:true,
      alertObject:{ 
        alert: true
        },
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style  scoped>
  .alert {
    background-color: chartreuse;
    width: 100%;
    height: 30px;
  }
</style> 
<!--We cant use interpolation in attributes of html 34 min timestamp -->
