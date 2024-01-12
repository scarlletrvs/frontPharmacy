<template>
<div class="card">
<p style="font-size: 14px; font-weight: bold;">
    nome da farmacia
</p>
<p style="font-size: 12px; font-weight: bold;">
    endereço
</p>
<p style="font-size: 12px; font-weight: bold;">
   ditancia em metros
</p> 

<buttonWhatsapp/>


</div>
  
</template>


<style>

.card{
    display: flex;
    align-items: center;
    height: auto;
    width: 160px;
    background-color: aquamarine;
    flex-direction: column;
}
</style>


<script >
import buttonWhatsapp  from './buttonwhatsapp.vue';

export default{
  components:{
    buttonWhatsapp
  }
}
</script>