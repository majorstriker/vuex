<template>
  <div id="app" class="center">
    <HeaderComp />
    <div><img class="header" src="./assets/top.jpg"></div>
    <ProjectDetails />
    <div class="attach">
            <div class="slider_case">
                <v-slider v-bind="options">
                    <div class="item"><img src="./assets/slider.jpg"></div>
                    <div class="item"><img src="./assets/slider.jpg"></div>
                    <div class="item"><img src="./assets/slider.jpg"></div>
                </v-slider>
            </div>

        </div>
    <FooterComp />
  </div>
</template>

<script>
import HeaderComp from './components/Header.vue'
import FooterComp from './components/Footer.vue'
import slider from './components/slider.vue'
import ProjectDetails from './components/ProjectDetails.vue'

export default {
  name: 'App',
  components: {
    HeaderComp,
    ProjectDetails,
    'v-slider': slider,
    FooterComp    
  },
  methods: {

    
  },
  computed: {
    details () {
      return this.$store.state.projectDetails
    }
  }

}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Lato', sans-serif;
}

img {
  max-width: 100%;
}

a {
  text-decoration: none;
}

.center {
  padding-left: calc(50% - 570px);
  padding-right: calc(50% - 570px);
}

.header {
  display: block;
  width: 100%;
}
.attach {
        width: 100%;
        max-width: 1000px;
        min-width: 480px;
        padding: 50px 15px;
        margin: 0 auto;
        position: relative;
    }

    .slider_case {
        margin-bottom: 40px;
    }

    .item {
      flex-shrink: 0;
      border-radius: 70px;
    }

</style>