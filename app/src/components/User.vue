<template>
  <li>
    <div class="title">
      <h3>User: {{user.email}}</h3>
      <div v-for="(goal, i) in user.goals" :key="goal.description">
      <p> GOAL #{{i+1}}: {{goal.description}}</p>
      </div>
    </div>
  </li>
</template>

<script>
export default {
  props: {
    user: Object
  }
};
</script>

<style scoped>
body {
  font-family: 'Open Sans';
}
li {
  list-style: none;
}
h3 {
  color: red;
}
/*
h3{
  font-family:'Playfair Display';
  font-size:25px;
  letter-spacing: 1px;
  color:white;
  margin-bottom:0;
  text-transform: none;
}
p {
  margin-top: 15px;
  font-size: 10px;
  text-transform: uppercase;
  letter-spacing: 2px;
  text-align: center !important;
}
.title-bg {
  background: black;
  color:white;
  position: absolute;     
  text-align: center;  
  padding: 0px 20px 10px 20px;  
  bottom: 0px; 
  width: 100%;
} */
</style>