<template>
  <div id="app">

    <nav class="navbar navbar-expand-md navbar-light bg-light">
      <a class="navbar-brand" href="#"><img src="./assets/images/logo.png" height="40px" alt="Grupo 107"></a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav ml-auto">
          <li class="nav-item active">
            <a class="nav-link" href="#">Inicio</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#services">Servicios</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#music">Música</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#news">Noticias</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#team">Equipo</a>
          </li>
        </ul>
      </div>
    </nav>

    <div class="container">
      <!-- Carousel Banners -->
      <div id="bannerId" class="carousel slide mb-4" data-ride="carousel">
        <ol class="carousel-indicators">
          <li data-target="#bannerId" data-slide-to="0" class="active"></li>
          <li data-target="#bannerId" data-slide-to="1"></li>
          <li data-target="#bannerId" data-slide-to="2"></li>
        </ol>
        <div class="carousel-inner" role="listbox">
          <div class="carousel-item active">
            <img src="./assets/images/banner1.jpg" class="d-block w-100" alt="Banner 1">
            <div class="carousel-caption d-none d-md-block">
              <h4>Servicios</h4>
              <p>Convenios con las mejores empresas.</p>
            </div>
          </div>
          <div class="carousel-item">
            <img src="./assets/images/banner2.jpg" class="d-block w-100" alt="Second slide">
          </div>
          <div class="carousel-item">
            <img src="./assets/images/banner3.jpg" class="d-block w-100" alt="Third slide">
          </div>
        </div>
        <a class="carousel-control-prev" href="#bannerId" role="button" data-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="sr-only">Previous</span>
        </a>
        <a class="carousel-control-next" href="#bannerId" role="button" data-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="sr-only">Next</span>
        </a>
      </div>

      <main>

        <!-- Componente API MÚSICA -->
        <ServiciosTele></ServiciosTele>

      <!-- Sección de SERVICIOS -->
        <MisServicios></MisServicios>


        <!-- Inicio sección de noticias -->
        <div id="news" class="mb-3 mt-3">
          <h2 class="text-center mb-3">Últimas noticias</h2>

          <!-- Select de paises -->
          <div class="col-md-8 mx-auto mb-3">
            <div class="d-flex justify-content-between align-items-baseline">
              <label for="country" class="mb-2 mr-sm-2">Pais: </label>
              <select id="country" class="custom-select mb-2" v-model="country" @change="loadNews">
                <option v-for="country in countries" :key="country.value" :value="country.value">{{ country.name }}</option>
              </select>
            </div>
          </div>

          <!-- Cards con las 4 paises de noticias -->
          <div class="row row-cols-1 row-cols-md-2" v-if="news.length">
            <news-card :item="news[0]" />
            <news-card :item="news[1]" />
            <news-card :item="news[2]" />
            <news-card :item="news[3]" />
          </div>
        </div>
        <!-- Fin seccion de noticias -->

        <!-- Inicio sección de Equipo -->
        <div id="team" class="mb-3">
          <h2 class="text-center mb-3">Nuestro equipo</h2>
          <div class="row" >
            <team-card v-for="member in members" v-bind:key="member.codigo" v-bind:member="member"></team-card>
          </div>
        </div>
        <!-- Fin sección de equipo -->
      </main>
    </div>

    <!-- Pie de página -->
    <div class="container-fluid bg-secondary text-white">
      <footer class="container py-3">
        <div class="row">
          <div class="col-md-6">
            <h4 class="footer-info-title">Grupo 107</h4>
            <p>Este sitio ofrece servicios desde el área de las telecomunicaciones en convenio con las mejores empresas del sector, y se enfoca en brindar un excelente servicio al cliente y es desarrollado por nuestro equipo.</p>
            <a href="https://github.com/MinTIC-Group-107/semana-2-107" class="btn btn-outline-light"><i class="fab fa-github"></i> Ver en GitHub</a>
          </div>
          <div class="col-md-6">
            <h4>Contacto</h4>
            <ul>
              <footer-member v-for="member in members" :key="member.codigo" :member="member"/>
            </ul>
          </div>
        </div>
        <div class="text-center bg-gray py-2">
          <p class="mb-0">&copy; 2020 - MinTIC - Universidad Tecnológica de Pereira - <strong>Grupo 107</strong></p>
        </div>
      </footer>
    </div>
  </div>
</template>

<script>
import MisServicios from './components/MisServicios.vue'
import ServiciosTele from './components/ServiciosTele.vue'
import FooterMember from './components/FooterMember'
import TeamCard from './components/TeamCard.vue'
import NewsCard from './components/NewsCard'

import axios from 'axios'
import members from './members'

export default {
  components: { TeamCard, FooterMember, MisServicios, ServiciosTele, NewsCard },
  name: 'App',
  data() {
    return {
      members: [],
      news: [],
      country: 'co',
      countries: [
        { value: "ar", name: "Argentina" },
        { value: "br", name: "Brasil" },
        { value: "ca", name: "Canadá" },
        { value: "co", name: "Colombia" },
        { value: "cl", name: "Chile" },
        { value: "cn", name: "China" },
        { value: "ec", name: "Ecuador" },
        { value: "es", name: "España" },
        { value: "us", name: "Estados Unidos" },
        { value: "mx", name: "México" },
        { value: "ve", name: "Venezuela" }
      ]
    }
  },
  created() {
    this.members = members
    this.loadNews()
  },
  methods: {
    loadNews() {
      let apiKey = process.env.VUE_APP_API_NEWS_KEY;
      let url = `http://api.mediastack.com/v1/news?access_key=${apiKey}&countries=${this.country}`

      axios.get(url)
        .then(response => {
          this.news = response.data.data
        })
        .catch(error => {
          console.log('Hubo un problema cargando las noticias desde la API.', error.response.data)
        })
    }
  }
}
</script>

