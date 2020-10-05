<template lang="html">
  <div>
    <navbar></navbar>
  </div>
</template>

<script>
import axios from 'axios';
import env from '../config/env';
import AlbumCard from "~/components/albumCard";
import navbar from "@/components/navbar";

export default {
  name: 'PruebaNuxt',
  components: {AlbumCard, navbar},
  data() {
    return {
      albums: []
    }
  },
  created() {
    let data = {
      email_address: 'test_comunal@comunal.com',
      password: 'Test_Comunal123'
    }
    axios.get(`${env.login}`, {
      headers: {
        'Access-Control-Allow-Origin': "*",
        'Content-type': 'application/json'
      },
      data
    }).then(response => {
      console.log(response)
    });
  }
}
</script>

<style scoped>
.card {
  background-color: white;
  border: 22px;
  box-shadow: #47494e;
  margin-bottom: 20px;
}
</style>
