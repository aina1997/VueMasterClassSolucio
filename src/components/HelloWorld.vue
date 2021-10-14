<template>
  <div class="container">
    <h1>Aquesta és la pàgina principal</h1>
    <div class="row">
      <ButtonCustom 
        v-for="btn in buttonList" :key="btn.id" 
        :nom="btn.name" 
        :text="btn.test"
        :classBnt="btn.class"
        @change="sumaUn"
      >Text slot<br></ButtonCustom>
    </div>
    <div class="row">
      <div class="col-md-4"></div>
      <div class="col-md-4"><h1 class="mt-5 p-3">{{sumatori}}</h1></div>
      <div class="col-md-4"></div>
    </div>
  </div>
</template>



<script>

import ButtonCustom from './Button.vue';
export default {
  name: 'PaginaPrincipal',
  components: {
    ButtonCustom
  },
  data(){
    return{
      sumatori: 0,
      buttonList: 
        [
          {name: "Patata", id:1, test:"Hola", class:"btn-outline-primary"},
          {name: "Floreta", id:2, test:"Hola", class:"btn-outline-danger"},
          {name: "Cargol", id:3, test:"Hola", class:"btn-primary"}
        ]
    }
  },
  methods: {
    sumaUn() {
      this.sumatori ++;
    }
  }
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
