

<template class="body">
  <div class="cards">
    <cardFarmacia/>
  </div>
 
</template>

<style>
.cards{
  display: flex;
  justify-content: flex-start;
  align-items: flex-start;
  height: 100vh;
  width: 100vw;

}

.body{
  display: flex;
  flex-direction: column;
 
}
</style>



<script >
import cardFarmacia from './components/cardFarmacia.vue';
export default{
  components:{
    cardFarmacia,
  }
}
</script>