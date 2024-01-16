<template>
  <div class="card">
    <p style="font-size: 14px; font-weight: bold;">
      Nome da Farmácia
    </p>
    <p style="font-size: 12px; font-weight: bold;">
      Endereço
    </p>
    <p style="font-size: 12px; font-weight: bold;">
      Distância em metros
    </p>

    <input type="text" placeholder="Digite sua localização">

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
    gap: 5px;
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