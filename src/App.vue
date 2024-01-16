<!-- body.vue -->

<template class="body">
  <div class="cards">
    <cardFarmacia/>
  </div>
</template>

<style>
.cards {
  display: flex;
  justify-content: flex-start;
  align-items: flex-start;
  height: 100vh;
  width: 100vw;
}

.body {
  display: flex;
  flex-direction: column;
}
</style>

<script>
import cardFarmacia from './components/cardFarmacia.vue';

export default {
  components: {
    cardFarmacia,
  },
  mounted() {
    this.askForLocationPermission();
  },
  methods: {
    askForLocationPermission() {
      if ('geolocation' in navigator) {
        navigator.geolocation.getCurrentPosition(
          this.handleLocationSuccess,
          this.handleLocationError
        );
      } else {
        alert('Geolocalização não é suportada pelo seu navegador.');
      }
    },
    handleLocationSuccess(position) {
      const latitude = position.coords.latitude;
      const longitude = position.coords.longitude;

      // Aqui você pode fazer o que quiser com a latitude e longitude
      alert(`Latitude: ${latitude}, Longitude: ${longitude}`);
    },
    handleLocationError(error) {
      switch (error.code) {
        case error.PERMISSION_DENIED:
          alert('Permissão para geolocalização negada pelo usuário.');
          break;
        case error.POSITION_UNAVAILABLE:
          alert('Informações de localização indisponíveis.');
          break;
        case error.TIMEOUT:
          alert('A solicitação para obter a localização do usuário excedeu o tempo limite.');
          break;
        default:
          alert('Erro desconhecido ao obter a localização do usuário.');
      }
    },
  },
};
</script>
