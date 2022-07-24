<script>
import Paket from './Paket.vue';

export default {
  components: { Paket },
  data() {
    return {
      pilihanPaket: [
        {
          title: 'Teman Dekat',
          price: 'Free',
          desc: 'Paket Spesial (Tapi Gak Pake Telor) Untuk Kamu TEMAN DEKAT dari owner fynjoki',
          keuntungan: [
            'Prioritas Joki Level 3',
            'Dijokiin Kalo Mood Doang',
            'Diroasting',
            'Dikasih Tutor Deck',
            'Kadang Kode Lu Diacak',
            'Folder Tugas Lu Dihapus'
          ]
        },
        {
          title: 'Berduit',
          price: 'Rp 450K / Bulan',
          desc: 'Pas untuk kamu yang baru pengen nyoba nyoba layanan kami (gak usah protes mahal).',
          keuntungan: [
            'Prioritas Joki Level 2',
            'Maksimal 5 Tugas / Minggu',
            'Diingetin Waktu Imsak',
            'Membuat Percaya Diri',
            'Terhindar Dari Zina',
            'Bisa Curhat Masalah Cinta',
            'Imun Tubuh Meningkat'
          ]
        },
        {
          title: 'Anak Raffi Ahmad',
          price: 'Rp 1M / Bulan',
          desc: 'Beda dikit dari paket berduit cuman lebih mahal aja (sama tambahan keuntungan dikit)',
          keuntungan: [
            'Prioritas Joki Level 1',
            'Maksimal 10 Tugas / Minggu',
            'Dianterin Kalo Jajan Ke Kantin',
            'Ditemenin Sleepcall Sampe Ileran',
            'Dapet Bundle FF Terbaru',
            'Ditutorin Jadi Hengker',
            'Lisensi Musik Idon Sepeg',
            'Dinyanyiin Jancok Pristel'
          ]
        },
      ]
    }
  }
}
</script>

<template>
  <div id="Harga">
    <div class="header">
      <h2>Berikut Beberapa Pilihan Paket Yang Bisa Lu Pilih</h2>
      <p>
        Dibawah ini pilihan paket paket yang bisa lu pilih. Makin mahal harganya makin banyak 
        keuntungan yang lu dapetin (jelas lah).
      </p>
    </div>
    <div class="daftarPaket">
      <Paket v-for="paket in pilihanPaket" :paket="paket" />
    </div>
    <div>
      <p>
        Gak Tertarik Sama Pilihan Paket Yang Disediain di Atas? Tenang! Lu Masih Bisa 
        Pilih Buat Bayar Joki / Tugas Dengan Harga Yang Bisa Dinegosiasiin (Awas Aja Kalo Murah Banget Nawarnya).
      </p>
    </div>
  </div>
</template>

<style scoped>
#Harga {
  margin-top: 80px;
  background-color: rgba(131, 86, 190, 0.2);
  padding: 60px 35px;
}

#Harga .header {
  text-align: center;
}

#Harga .header h2 {
  font-size: 1.5em;
}

#Harga .header p {
  font-weight: 700;
  color: rgb(109, 109, 109);
  width: 100%;
  margin: 15px auto;
  font-size: 1.1em;
  max-width: 600px;
}

#Harga .daftarPaket {
  margin-top: 60px;
  display: flex;
  justify-content: space-around;
  align-items: flex-start;
  flex-wrap: wrap;
}

#Harga .daftarPaket ~ div:last-child {
  width: 100%;
  text-align: center;
  margin: 30px auto;
  max-width: 600px;
}

#Harga .daftarPaket ~ div:last-child p {
  font: normal bolder 1.3em/30px 'Dosis', sans-serif;
  color: #646464;
}

@media (max-width:950px) {
  #Harga {
    margin-top: 50px;
    background-color: rgba(131, 86, 190, 0.2);
    padding: 60px 20px;
  }
}

@media (max-width: 425px) {
  #Harga .daftarPaket ~ div:last-child p {
    font: normal 600 1.2em/31px 'Dosis', sans-serif;
    color: #646464;
  }
}
</style>