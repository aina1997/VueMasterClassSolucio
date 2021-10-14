<template>
  <div class="col-md-4">
    <div class="card m50 p50">
      <div class="card-body">
        <h5 class="card-title">{{nom}}</h5>
        <p class="card-text">{{text}}</p>
        <slot></slot>
        <a href="#" class="btn" :class="classBnt" @click="numberOfClicks++; $emit('change', numberOfClicks)" v-bind:style="{ backgroundColor: colors[numberOfClicks%colors.length]}">Dale</a>
      </div>
      <button></button>
    </div>
  </div>
  
</template>

<script>
export default {
  name: 'ButtonCustom',
  props:[
    'nom', 'text', 'classBnt'
  ],
  data() {
    return{
      colors: ['null','red', 'pink', 'blue', 'cyan', 'green', 'yellow'],
      numberOfClicks: 0
    }
  }
}
</script>

