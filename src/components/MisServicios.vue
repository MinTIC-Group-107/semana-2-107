<template>
  <!-- Inicio sección MUSIC -->
            <div class="container">
                <h2 class="text-center mb-3">Escucha tu música preferida</h2>
                <div class="row">
                    <template>

                        <div class="col-sm-4" v-for="item in info" :key="item.id">
                            <div class="card">
                                <img :src="'https://www.dailymotion.com/thumbnail/video/' + item.id" alt=""
                                    class="car-img-top">
                                <div class="card-body">
                                    <h5 class="card-title">{{item.title}}</h5>
                                    <a v-bind:href="'https://www.dailymotion.com/video/' + item.id"
                                        class="btn btn-primary">Reproducir</a>

                                </div>
                            </div>
                        </div>
                    </template>

                </div>

            </div>

</template>




<script>
import axios from'axios'
export default {
    data(){
        return{
            info: []
        }
    },

    mounted(){
            axios.get("https://api.dailymotion.com/videos?channel=music&limit=3")
                            .then(respuesta => this.info = respuesta.data.list)
    }
}
</script>
