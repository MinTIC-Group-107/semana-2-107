<template>
  <div id="app">

    <nav class="navbar navbar-expand-md navbar-light bg-light">
      <a class="navbar-brand" href="#"><img src="/images/logo.png" height="40px" alt="Grupo 107"></a>
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
            <img src="/images/banner1.jpg" class="d-block w-100" alt="Banner 1">
            <div class="carousel-caption d-none d-md-block">
              <h4>Servicios</h4>
              <p>Convenios con las mejores empresas.</p>
            </div>
          </div>
          <div class="carousel-item">
            <img src="/images/banner2.jpg" class="d-block w-100" alt="Second slide">
          </div>
          <div class="carousel-item">
            <img src="/images/banner3.jpg" class="d-block w-100" alt="Third slide">
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
        <div id="news" class="mb-3">
          <h2 class="text-center mb-3">Noticias</h2>
          <div class="row row-cols-1 row-cols-md-2">
            <div class="col mb-2">
              <div class="card shadow mb-3">
                <div class="row no-gutters">
                  <div class="col-lg-5">
                    <img src="/images/telefonia2.jpg" class="card-img" alt="Telefonia 2">
                    <div class="card-body">
                      <h4 class="card-title">Colombian-os pueden aplicar desde hoy a portabilidad móvil</h4>
                    </div>
                  </div>
                  <div class="col-lg-7">
                    <div class="card-body">
                      <p class="card-text">Los usuarios de servicios móviles en Colombia podrán cambiar de operador sin modificar su número en 24 horas desde este miércoles. Según cifras de la Comisión de Regulación de Comunicaciones (CRC), citadas por Tigo, a corte de junio de 2019 se realizaron cerca de 20,3 millones de portaciones desde 2011, cuando se implementó esta medida.</p>
                      <hr>
                      <p class="card-text"><a href="https://www.dinero.com/empresas/confidencias-on-line/articulo/portabilidad-movil-en-un-dia-comienza-este-miercoles-1-de-julio/291188" class="btn btn-link">Leer noticia completa >></a></p>
                    </div>
                  </div>
                </div>
              </div>
              </div>
              <div class="col mb-2">
                <div class="card shadow mb-3">
                  <div class="row no-gutters">
                    <div class="col-lg-5">
                      <img src="/images/telefonia1.jpg" class="card-img" alt="Telefonia 1">
                      <div class="card-body">
                        <h4 class="card-title">Google anunciará en voz alta quién está llamando</h4>
                      </div>
                    </div>
                    <div class="col-lg-7">
                      <div class="card-body">
                        <p class="card-text">Google está probando nuevas funciones en su aplicación Teléfono de Google, para identificar en voz alta el nombre la persona que llama, sin necesidad así de tener que mirar la pantalla. Asimismo, Teléfono de Google prueba también otras novedades como la posibilidad de borrar automáticamente, después de 30 días, ...</p>
                        <hr>
                        <p class="card-text"><a href="https://www.dinero.com/empresas/confidencias-on-line/articulo/google-se-prepara-para-que-su-telefono-anuncie-en-voz-alta-quien-llama/301925" class="btn btn-link">Leer noticia completa >></a></p>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
              <div class="col mb-2">
                <div class="card shadow mb-3">
                  <div class="row no-gutters">
                    <div class="col-lg-5">
                      <img src="/images/telefonia3.jpg" class="card-img" alt="Telefonia 3">
                      <div class="card-body">
                        <h4 class="card-title">¿Qué están haciendo los operadores para evitar un colapso en la red?</h4>
                      </div>
                    </div>
                    <div class="col-lg-7">
                      <div class="card-body">
                        <p class="card-text">Empresas de telecomunicaciones ya adoptaron medidas en sus servicios de red por el coronavirus.</p>
                        <p class="card-text">Este viernes se inició el simulacro de cuarentena en Bogotá y también en diferentes regiones del país. Y ya desde hace algunas semanas miles de trabajadores empezaron a trabajar de forma remota desde sus casas. Esto, sin dudas, hace que el número de usuarios en simultáneo que están conectados a la red aumente.</p>
                        <hr>
                        <p class="card-text"><a href="https://www.eltiempo.com/tecnosfera/novedades-tecnologia/coronavirus-como-esta-funcionando-el-internet-en-colombia-por-teletrabajo-475240" class="btn btn-link">Leer noticia completa >></a></p>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
              <div class="col mb-2">
                <div class="card shadow mb-3">
                  <div class="row no-gutters">
                    <div class="col-lg-5">
                      <img src="/images/television.jpg" class="card-img" alt="Televisión">
                      <div class="card-body">
                        <h4 class="card-title">Así creció el consumo de televisión en Colombia en 2020</h4>
                      </div>
                    </div>
                    <div class="col-lg-7">
                      <div class="card-body">
                        <p class="card-text">El consumo de televisión en Colombia ha sido más alto en 2020 que el registrado en 2019, según reveló el estudio de audiencias de Kantar Ibope Media sobre el rating y consumo de ese medio. En agosto del año pasado los colombianos veían un promedio de 4 horas 14 minutos, mientras que en ese mismo mes de este año ven 4 horas 41 minutos, es decir 27 minutos más de televisión...</p>
                        <hr>
                        <p class="card-text"><a href="https://www.dinero.com/noticias/television/417" class="btn btn-link">Leer noticia completa >></a></p>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
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
            <a href="https://github.com/MinTIC-Group-107/sprint1-bootstrap" class="btn btn-outline-light"><i class="fab fa-github"></i> Ver en GitHub</a>
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
import axios from 'axios'

export default {
  components: { TeamCard, FooterMember, MisServicios, ServiciosTele },
  name: 'App',
  data() {
    return {
      members: []
    }
  },
  created() {
    axios.get('members.json')
      .then(datos => {
        this.members = datos.data
      }).catch(error => {
        console.log('No se pudieron cargar los datos de los miembros de equipo.', error)
      })
  }
}
</script>

