<template>
  <div class="flex h-full">
    <Nav @Home="activeHome" @About="activeAbout" @Portfolio="activePortfolio" @News="activeNews" @Contact="activeContact" />
    <ProfileHome v-if="HomeShow" />
    <About v-if="AboutShow"/>
    <Portfolio v-if="Portfolio" />
    <News v-if="News"/>
    <Contact v-if="Contact" />
  </div>
</template>

<script>
import Nav from '../components/Nav';
import ProfileHome from '../components/ProfileHome';
import About from '../components/About';
import Portfolio from '../components/Portfolio';
import News from '../components/News';
import Contact from '../components/Contact';

export default {
  data(){
    return{
      HomeShow:true,
      AboutShow:false,
      Portfolio:false,
      News:false,
      Contact:false
    }
  },
  components: {
    Nav , ProfileHome , About , Portfolio , News , Contact
  },
  methods:{
    activeHome() {
      this.HomeShow = true
      this.AboutShow = false
      this.Portfolio = false
      this.News = false
      this.Contact = false
    },
    activeAbout() {
      this.AboutShow = true
      this.HomeShow = false
      this.Portfolio = false
      this.News = false
      this.Contact = false
    },
    activePortfolio() {
      this.AboutShow = false
      this.HomeShow = false
      this.Portfolio = true
      this.News = false
      this.Contact = false
    },
    activeNews() {
      this.AboutShow = false
      this.HomeShow = false
      this.Portfolio = false
      this.News = true
      this.Contact = false
    },
    activeContact() {
      this.AboutShow = false
      this.HomeShow = false
      this.Portfolio = false
      this.News = false
      this.Contact = true
    }
  }
}
</script>
