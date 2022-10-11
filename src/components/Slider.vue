<template>
  <div id="carouselExampleControls" class="carousel slide bs-slider box-slider" data-ride="carousel" data-pause="hover" data-interval="false" >
    <!-- Indicators -->
    <ol class="carousel-indicators">
      <li data-target="#carouselExampleControls" data-slide-to="0" class="active"></li>
      <li data-target="#carouselExampleControls" data-slide-to="1"></li>
      <li data-target="#carouselExampleControls" data-slide-to="2"></li>
    </ol>


    <div class="carousel-inner" role="listbox">
      <div v-if="sliders.length > 0">
        <div class="carousel-item" v-for="(slider, id) in sliders" :class="{ active: id==0 }" :key='slider.id'>
          <img :src="slider.image" class="w-100"
               style="height:400px;object-fit:cover">
        </div>
      </div>
      <div v-else class="mt-5">
        <div class="card border-0 shadow-sm rounded-lg mb-3" v-for="loader in sliders_loader" :key="loader">
          <div class="card-body pt-4">
            <ContentLoader />
          </div>
        </div>
      </div>

<!--      <div class="carousel-item active">-->
<!--        <div id="home" class="first-section" style="background-image:url('images/slider-01.jpg');">-->
<!--          <div class="dtab">-->
<!--            <div class="container">-->
<!--              <div class="row">-->
<!--                <div class="col-md-12 col-sm-12 text-right">-->
<!--                  <div class="big-tagline">-->
<!--                    <h2><strong>SmartEDU </strong> education College</h2>-->
<!--                    <p class="lead">With Landigoo responsive landing page template, you can promote your all hosting, domain and email services. </p>-->
<!--&lt;!&ndash;                    <a href="#" class="hover-btn-new"><span>Contact Us</span></a>&ndash;&gt;-->
<!--                    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-->
<!--&lt;!&ndash;                    <a href="#" class="hover-btn-new"><span>Read More</span></a>&ndash;&gt;-->
<!--                  </div>-->
<!--                </div>-->
<!--              </div>&lt;!&ndash; end row &ndash;&gt;-->
<!--            </div>&lt;!&ndash; end container &ndash;&gt;-->
<!--          </div>-->
<!--        </div>&lt;!&ndash; end section &ndash;&gt;-->
<!--      </div>-->

<!--      <div class="carousel-item">-->
<!--        <div id="home" class="first-section" style="background-image:url('images/slider-02.jpg');">-->
<!--          <div class="dtab">-->
<!--            <div class="container">-->
<!--              <div class="row">-->
<!--                <div class="col-md-12 col-sm-12 text-left">-->
<!--                  <div class="big-tagline">-->
<!--                    <h2 data-animation="animated zoomInRight">SmartEDU <strong>education school</strong></h2>-->
<!--                    <p class="lead" data-animation="animated fadeInLeft">With Landigoo responsive landing page template, you can promote your all hosting, domain and email services. </p>-->
<!--                    <a href="#" class="hover-btn-new"><span>Contact Us</span></a>-->
<!--                    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-->
<!--                    <a href="#" class="hover-btn-new"><span>Read More</span></a>-->
<!--                  </div>-->
<!--                </div>-->
<!--              </div>&lt;!&ndash; end row &ndash;&gt;-->
<!--            </div>&lt;!&ndash; end container &ndash;&gt;-->
<!--          </div>-->
<!--        </div>&lt;!&ndash; end section &ndash;&gt;-->
<!--      </div>-->

<!--      <div class="carousel-item">-->
<!--        <div id="home" class="first-section" style="background-image:url('images/slider-03.jpg');">-->
<!--          <div class="dtab">-->
<!--            <div class="container">-->
<!--              <div class="row">-->
<!--                <div class="col-md-12 col-sm-12 text-center">-->
<!--                  <div class="big-tagline">-->
<!--                    <h2 data-animation="animated zoomInRight"><strong>VPS Servers</strong> Company</h2>-->
<!--                    <p class="lead" data-animation="animated fadeInLeft">1 IP included with each server-->
<!--                      Your Choice of any OS (CentOS, Windows, Debian, Fedora)-->
<!--                      FREE Reboots</p>-->
<!--                    <a href="#" class="hover-btn-new"><span>Contact Us</span></a>-->
<!--                    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-->
<!--                    <a href="#" class="hover-btn-new"><span>Read More</span></a>-->
<!--                  </div>-->
<!--                </div>-->
<!--              </div>&lt;!&ndash; end row &ndash;&gt;-->
<!--            </div>&lt;!&ndash; end container &ndash;&gt;-->
<!--          </div>-->
<!--        </div>&lt;!&ndash; end section &ndash;&gt;-->
<!--      </div>-->

      <!-- Left Control -->
      <a class="new-effect carousel-control-prev" href="#carouselExampleControls" role="button" data-slide="prev">
        <span class="fa fa-angle-left" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
      </a>

      <!-- Right Control -->
      <a class="new-effect carousel-control-next" href="#carouselExampleControls" role="button" data-slide="next">
        <span class="fa fa-angle-right" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
      </a>
    </div>
  </div>
</template>

<script>
//import content loader
import {
  ContentLoader
} from 'vue-content-loader';

//import axios
import axios from 'axios';

//import hook onMounted from vue
import { ref, onMounted } from 'vue';

export default {
  name: 'SliderComponent',

  components: {
    //loader component
    ContentLoader
  },

  setup() {

    //define state
    const sliders = ref([]);

    //define state
    const sliders_loader = ref(1);

    //on mounted
    onMounted(() => {
      //get data
      axios.get('/api/slider')
          .then(response => {
            //set data
            sliders.value = response.data.data.data;
          })
          .catch(() => {
            //set data
            sliders.value = [];
          });
    });

    //return data
    return {
      sliders,
      sliders_loader
    }

  }

}
</script>

