<template>
<div class="col mb-2">
  <div class="card shadow mb-3">
    <div class="row no-gutters">
      <div class="col-lg-7">
        <img :src="item.urlToImage" class="card-img" :alt="item.title" v-if="item.urlToImage">
        <div class="card-body">
          <h5 class="card-title">{{ item.title }}</h5>
        </div>
      </div>
      <div class="col-lg-5">
        <div class="card-body">
          <p class="card-text">{{ item.content }}</p>
          <hr>
          <p class="card-text"><a :href="item.url" class="btn btn-link">Leer noticia completa >></a></p>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  props: ["item"]
}
</script>
