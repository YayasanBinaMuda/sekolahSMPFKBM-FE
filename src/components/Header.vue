<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container-fluid">

        <!-- <img src="images/logo.png" alt="" /> -->
        <router-link :to="{name: 'home'}" class="navbar-brand"><i class="fa fa-graduation-cap" aria-hidden="true"></i> 
          SMP FK Bina Muda</router-link>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbars-host" aria-controls="navbars-rs-food" aria-expanded="false" aria-label="Toggle navigation">
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbars-host">
       <!--  <ul class="navbar-nav ml-auto">
          <li class="nav-item active"><a class="nav-link" href="index.html">Home</a></li>
          <li class="nav-item"><a class="nav-link" href="about.html">About Us</a></li>
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" id="dropdown-a" data-toggle="dropdown">Course </a>
            <div class="dropdown-menu" aria-labelledby="dropdown-a">
              <a class="dropdown-item" href="course-grid-2.html">Course Grid 2 </a>
              <a class="dropdown-item" href="course-grid-3.html">Course Grid 3 </a>
              <a class="dropdown-item" href="course-grid-4.html">Course Grid 4 </a>
            </div>
          </li>
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" id="dropdown-a" data-toggle="dropdown">Blog </a>
            <div class="dropdown-menu" aria-labelledby="dropdown-a">
              <a class="dropdown-item" href="blog.html">Blog </a>
              <a class="dropdown-item" href="blog-single.html">Blog single </a>
            </div>
          </li>
          <li class="nav-item"><a class="nav-link" href="teachers.html">Teachers</a></li>
          <li class="nav-item"><a class="nav-link" href="pricing.html">Pricing</a></li>
          <li class="nav-item"><a class="nav-link" href="contact.html">Contact</a></li>
        </ul>
        <ul class="nav navbar-nav navbar-right">
          <li><a class="hover-btn-new log orange" href="#" data-toggle="modal" data-target="#login"><span>Book Now</span></a></li>
        </ul> -->
        <ul class="navbar-nav mr-auto mb-2 mb-md-0">
                    <li class="nav-item">
                        <router-link :to="{name: 'post'}" class="nav-link"><i class="fa fa-book-open" aria-hidden="true"></i> BERITA</router-link>
                    </li>
                    <li class="nav-item">
                        <router-link :to="{name: 'event'}" class="nav-link"><i class="fa fa-calendar" aria-hidden="true"></i> AGENDA</router-link>
                    </li>
                    <li class="nav-item">
                        <router-link :to="{name: 'photo'}" class="nav-link"><i class="fa fa-image" aria-hidden="true"></i> GALERI</router-link>
                    </li>
                    <li class="nav-item">
                        <router-link :to="{name: 'video'}" class="nav-link"><i class="fa fa-video" aria-hidden="true"></i> VIDEO</router-link>
                    </li>
                    <li class="nav-item">
                        <router-link :to="{name: 'contact'}" class="nav-link"><i class="fa fa-phone" aria-hidden="true"></i> KONTAK</router-link>
                    </li>
                </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'HeaderComponent'
}
</script>

