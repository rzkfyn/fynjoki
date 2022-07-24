<script>
import NavBar from './components/NavBar.vue';
import Beranda from './components/Beranda.vue';
import Line from './components/Line.vue';
import Kenapa from './components/Kenapa.vue';
import Harga from './components/Harga.vue';
import Testimoni from './components/Testimoni.vue';
import LastContent from './components/LastContent.vue';
import Footer from './components/Footer.vue';

export default {
  components: { NavBar, Beranda, Line, Kenapa, Harga, Testimoni, Footer, LastContent },
  data() {
    return {
      scrolled: window.scrollY > 0,
      activenav: ''
    }
  },
  methods: {
    checkScroll() {
      return this.scrolled = window.scrollY > 0
    },
    checkActiveNav(){
      const beranda = document.querySelector('#Beranda');
      const kenapa = document.querySelector('#Kenapa');
      const harga = document.querySelector('#Harga');
      const testimoni = document.querySelector('#Testimoni');
      
      const berandaLimit = 0 - beranda.clientHeight;
      const kenapaLimit = 0 - kenapa.clientHeight;
      const hargaLimit = 0 - harga.clientHeight;
      const testimoniLimit = 0 - testimoni.clientHeight;

      if (beranda.getBoundingClientRect().top < 100 && (beranda.getBoundingClientRect().top - 100) > berandaLimit) return this.activenav = 'beranda';
      if (kenapa.getBoundingClientRect().top < 100 && (kenapa.getBoundingClientRect().top - 100) > kenapaLimit) return this.activenav = 'kenapa';
      if (harga.getBoundingClientRect().top < 100 && (harga.getBoundingClientRect().top - 100) > hargaLimit) return this.activenav = 'harga';
      if (testimoni.getBoundingClientRect().top < 100 && (testimoni.getBoundingClientRect().top - 100) > testimoniLimit) return this.activenav = 'testimoni';
    }
  },
  mounted() {
    document.addEventListener('scroll', () => {
      this.checkActiveNav();
      this.checkScroll();
    });
  }
}
</script>

<template>
  <NavBar :scrolled="scrolled" :activenav="activenav" />
  <main>
    <Beranda/>
    <Line/>
    <Kenapa/>
    <Harga/>
    <Testimoni/>
    <LastContent/>
  </main>
  <Line/>
  <Footer/>
</template>

<style>
@import url(./App.css);
</style>
