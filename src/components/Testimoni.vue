<script>
import TestimoniCard from './TestimoniCard.vue';

export default {
  components: { TestimoniCard },
  data() {
    return {
      testimonis: [
        {
        name: 'Sajuna Inui',
        occupation: 'Mahasiswa & Cosplayer',
        feedback: '"Keren banget kack tugasku beres dalam sekejap mata aku jadi ingin tinggal di Meikarta!"',
        rating: 5,
        img: 'inui.jpg'
        },
        {
        name: 'Kobokan Aer',
        occupation: 'Pawang Hujan & Pencoding Handal',
        feedback: '"Pelayanan keren, penjokinya juga ganteng banget dan sopan banget suka bantuin ngeluarin motor."',
        rating: 5,
        img: 'kobokan.png'
        },
        {
        name: 'Bambang Gagal Png',
        occupation: 'Cowo Kulbet Asal Bogor',
        feedback: '"Harga mahal trus gw malah dicepuin joki disini lagi tolol. Untung abang abangnya ganteng."',
        rating: 3,
        img: 'kul.png'
        },
        {
        name: 'Sachi Umino',
        occupation: 'Mahasiswa & LemONTEa',
        feedback: '"Tugasku cepet beres dan nilaiku jadi baguss. Tapi sayang ga bisa bayar pake cara anu :("',
        rating: 3,
        img: 'sachi.jpg'
        },
        {
        name: 'Alex Uchiha',
        occupation: 'Mahasiswa Tataboga',
        feedback: '"Pelayanan baik, tugas selesai dengan baik, penjoki penjokinya juga baik. Cuman saya aja yang ga baik"',
        rating: 1,
        img: 'fm.jpg'
        },
        {
        name: 'Wibu Hengker Pro Tzy',
        occupation: 'Mahasiswa Fangay Epep',
        feedback: '"Game burik ga ada pintu yahaha hayyu. Tapi boong pal pale pal pale kena mental deck Yahahahaha Hayyu"',
        rating: 0,
        img: 'yoru.jpg'
        }
      ]
    }
  }
}
</script>

<template>
  <div id="Testimoni">
    <div class="header">
      <div class="title">
        <h2>Apa Sih Kata Mereka Yang Udah Pake Layanan Joki di Sini?</h2>
      </div>
      <div class="subtitle">
        <p>
          Ini Testinya Kagak Difilter Soalnya Kita Males. Jadi, Semuanya Sesuai Hati Nurani Pengguna Tanpa Rekayasa.
        </p>
      </div>
    </div>
    <div class="body">
      <TestimoniCard v-for="testimoni in testimonis" :testimoni="testimoni" />
    </div>
  </div>
</template>

<style scoped>
#Testimoni {
  background-color: rgba(231, 195, 255, 0.507);
  padding: 40px 35px;
}

#Testimoni .header {
  text-align: center;
  margin: 0 auto;
  width: 100%;
  max-width: 650px;
  color: #1f1e1e;
}

#Testimoni .header .title {
  font-size: 1.2em;
  margin-bottom: 25px;
}

#Testimoni .header .subtitle {
  font-size: 1.2em;
  color: rgb(110, 110, 110);
  font-family: 'Dosis' sans-serif;
  font-weight: 600;
}

#Testimoni .body {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  padding: 40px 35px;
}

@media (max-width: 950px) {
  #Testimoni {
    padding: 40px 10px;
  }

  #Testimoni .body {
    padding: 20px 0;
  }
}
</style>