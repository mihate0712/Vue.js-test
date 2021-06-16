<template>
  <div>
    <b-button variant="outline-primary" @click="getIp">IPを取得</b-button>
    <hr/>
    <div>Your IP: {{ipAddress}}</div>
    <br>
    <div>Json Data: {{jsonData}}</div>
  </div>
</template>

<script>
import axios from 'axios'

export default{
  name: 'TestAPP',
  data(){
    return{
      jsonData: '',
      ipAddress: '',
    }
  },
  methods: {
    getIp() {
      const url='https://httpbin.org/get';
      axios.get(url)
        .then((response) => {
          console.log(response.data);
          this.jsonData = response.data;
          this.ipAddress = response.data.origin;
        })
        .catch((e) => {
          alert(e);
        });
    }
  }
}
</script>

<style scoped>
</style>
