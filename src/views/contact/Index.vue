<template>
  <div class="post-index">
      <!-- header -->
      <Header />
      <!-- end header -->

      <!-- main content -->
      <header class="pt-5 border-bottom bg-light">
          <div class="container pt-md-1 pb-md-1">
              <h1 class="bd-title mt-4 font-weight-bold"><i class="fa fa-phone" aria-hidden="true"></i> KONTAK</h1>
              <p class="bd-lead">Kontak SMP FK Bina Muda.</p>
          </div>
      </header>

      <!-- breadcrumb -->
      <nav aria-label="breadcrumb">
          <ol class="breadcrumb">
              <li class="breadcrumb-item">
                  <router-link :to="{ name: 'home' }" class="text-decoration-none"><i class="fa fa-home"></i> Home
                  </router-link>
              </li>
              <li class="breadcrumb-item">
                  <router-link :to="{ name: 'contact' }" class="text-decoration-none"><i class="fa fa-phone"></i>
                      Kontak</router-link>
              </li>
          </ol>
      </nav>
      <!-- end breadcrumb -->

      <div class="container-fluid mt-5 mb-5">

          <div class="row">
              <div class="col-md-7">
                  <div class="card border-0 shadow-sm rounded">
                      <div class="card-body">
                         <!--  <iframe
                          
                              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d253840.4878845067!2d106.6894283352192!3d-6.229728025238589!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e69f3e945e34b9d%3A0x5371bf0fdad786a2!2sJakarta%2C%20Daerah%20Khusus%20Ibukota%20Jakarta!5e0!3m2!1sid!2sid!4v1594508000901!5m2!1sid!2sid"
                              width="100%" height="400" frameborder="0" style="border:0;" allowfullscreen=""
                              aria-hidden="false" tabindex="0"></iframe> -->

                              <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d15840.903804897735!2d107.8369357!3d-6.9826413!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x9810d711fd7bd873!2sSMP%20FK%20Bina%20Muda!5e0!3m2!1sid!2sid!4v1665631083595!5m2!1sid!2sid" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
                      </div>
                  </div>
              </div>
              <div class="col-md-5">
                  <div class="card border-0 shadow-sm rounded">
                      <div class="card-body">
                          <h3>KONTAK KAMI</h3>
                          <hr>
                          <p>
                              <i class="fa fa-map-marker" aria-hidden="true"></i> Jln Kapten Sangun No. 33 Cicalengka, Tenjolaya, Kec. Cicalengka, Kab. Bandung Prov. Jawa Barat
                          </p>
                          <p>
                              <i class="fas fa-phone"></i> (022) 7949415
                          </p>
                          <p>
                              <i class="fas fa-envelope"></i> info@smpfkbinamuda.sch.id
                          </p>
                      </div>
                  </div>
              </div>
          </div>
      </div>
      <!-- main content -->

      <!-- footer -->
      <Footer />
      <!-- end footer -->
  </div>
</template>

<script>
  //import component
  import Header from "@/components/Header";
  import Footer from "@/components/Footer";


  export default {
      name: 'ContactComponent',
      components: {
          Header,
          Footer
      }
  }
</script>