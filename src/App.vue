<template>
  <div id="app">
    <input type="text" v-model="text">
    <button @click="getAddress">住所自動入力</button>
    <p>Address :{{ }}</p>
  </div>
</template>

<script>
import axios from "axios";
export default {
  props: [""],
  data() {
    return {
    };
  },
  async created() {
    const getAddress = await axios.get(
      `https://api.openweathermap.org/data/2.5/weather?q=${this.city}&units=metric&appid=inLiNPQOtiWwVg8PhMuys0iOfWuxmIG4nroFizN`
    );
  }
};
</script>