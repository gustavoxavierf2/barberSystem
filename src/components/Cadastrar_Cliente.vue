<template>
    
        <v-main style="min-height: 768px; display: flex" class="Content">
            <h1>
                Ola mundo
            </h1>
        </v-main>    
    
</template>

<script lang="ts">
import App from '../App.vue'
import Vue from 'vue'

export default {
    components: {
        App
    }    
}


</script>

<style scoped>
.Content{
  background-color: black;
  opacity: 90%;
  background-image: url("../assets/BackGround.jpg");
  background-size:auto;
  margin-left: 180px;
}

</style>