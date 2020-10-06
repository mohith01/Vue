<template>
  <div class="hello">
    <div class="holder">
      <ul>
        <li v-for="(data, index) in skills" :key='index'>{{ index}}. {{data.skill}}</li>
      </ul>

      <p v-if="skills.length >= 1"> You have more than one skill</p>
      <p v-else> You have less than one skill sed"</p>

      <div v-bind:class="{ alert: showAlert, 'another-class':showClass}"></div>

      
       <br> 
       <hr>
       <div vbind:class="alertObject"></div> 
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
      showClass:true,
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
  .another-class {
    border: 5px solid black;
  }
</style> 
<!--We cant use interpolation in attributes of html 34 min timestamp -->
