<script>
import Kelebihan from './Kelebihan.vue';

export default {
  components: { Kelebihan },
  data() {
    return {
      kelebihan: [
        {
          icon: `<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="currentColor" class="bi bi-speedometer2" viewBox="0 0 16 16">
                  <path d="M8 4a.5.5 0 0 1 .5.5V6a.5.5 0 0 1-1 0V4.5A.5.5 0 0 1 8 4zM3.732 5.732a.5.5 0 0 1 .707 0l.915.914a.5.5 0 1 1-.708.708l-.914-.915a.5.5 0 0 1 0-.707zM2 10a.5.5 0 0 1 .5-.5h1.586a.5.5 0 0 1 0 1H2.5A.5.5 0 0 1 2 10zm9.5 0a.5.5 0 0 1 .5-.5h1.5a.5.5 0 0 1 0 1H12a.5.5 0 0 1-.5-.5zm.754-4.246a.389.389 0 0 0-.527-.02L7.547 9.31a.91.91 0 1 0 1.302 1.258l3.434-4.297a.389.389 0 0 0-.029-.518z"/>
                  <path fill-rule="evenodd" d="M0 10a8 8 0 1 1 15.547 2.661c-.442 1.253-1.845 1.602-2.932 1.25C11.309 13.488 9.475 13 8 13c-1.474 0-3.31.488-4.615.911-1.087.352-2.49.003-2.932-1.25A7.988 7.988 0 0 1 0 10zm8-7a7 7 0 0 0-6.603 9.329c.203.575.923.876 1.68.63C4.397 12.533 6.358 12 8 12s3.604.532 4.923.96c.757.245 1.477-.056 1.68-.631A7 7 0 0 0 8 3z"/>
                </svg>`,
          title: 'Proses Cepat',
          body: 'Proses pengerjaan akan cepat karena rata rata penjoki kami adalah <em>shaker</em> handal yang pasti kalo ngetik mah ez lah deck.'
        },
        {
          icon: `<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="currentColor" class="bi bi-currency-dollar" viewBox="0 0 16 16">
                  <path d="M4 10.781c.148 1.667 1.513 2.85 3.591 3.003V15h1.043v-1.216c2.27-.179 3.678-1.438 3.678-3.3 0-1.59-.947-2.51-2.956-3.028l-.722-.187V3.467c1.122.11 1.879.714 2.07 1.616h1.47c-.166-1.6-1.54-2.748-3.54-2.875V1H7.591v1.233c-1.939.23-3.27 1.472-3.27 3.156 0 1.454.966 2.483 2.661 2.917l.61.162v4.031c-1.149-.17-1.94-.8-2.131-1.718H4zm3.391-3.836c-1.043-.263-1.6-.825-1.6-1.616 0-.944.704-1.641 1.8-1.828v3.495l-.2-.05zm1.591 1.872c1.287.323 1.852.859 1.852 1.769 0 1.097-.826 1.828-2.2 1.939V8.73l.348.086z"/>
                </svg>`,
          title: 'Harga Merakyat',
          body: 'Harganya sangat bersahabat untuk kantong kamu yang serata dada loli. Ada beberapa pilihan paket yang bisa kamu pilih berdasarkan kebutuhan dan budgetmu.'
        },
        {
          icon: `<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="currentColor" class="bi bi-code-slash" viewBox="0 0 16 16">
                  <path d="M10.478 1.647a.5.5 0 1 0-.956-.294l-4 13a.5.5 0 0 0 .956.294l4-13zM4.854 4.146a.5.5 0 0 1 0 .708L1.707 8l3.147 3.146a.5.5 0 0 1-.708.708l-3.5-3.5a.5.5 0 0 1 0-.708l3.5-3.5a.5.5 0 0 1 .708 0zm6.292 0a.5.5 0 0 0 0 .708L14.293 8l-3.147 3.146a.5.5 0 0 0 .708.708l3.5-3.5a.5.5 0 0 0 0-.708l-3.5-3.5a.5.5 0 0 0-.708 0z"/>
                </svg>`,
          title: 'Menyesuaikan Style Code',
          body: 'Kodinganmu akan kami evaluasi untuk meniru cara kamu mengetik kode agar tidak terdeteksi joki oleh gurumu (Tapi kami kadang cepu kalo kamu pake jasa joki disini).'
        },
        {
          icon: `<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="currentColor" class="bi bi-star" viewBox="0 0 16 16">
                  <path d="M2.866 14.85c-.078.444.36.791.746.593l4.39-2.256 4.389 2.256c.386.198.824-.149.746-.592l-.83-4.73 3.522-3.356c.33-.314.16-.888-.282-.95l-4.898-.696L8.465.792a.513.513 0 0 0-.927 0L5.354 5.12l-4.898.696c-.441.062-.612.636-.283.95l3.523 3.356-.83 4.73zm4.905-2.767-3.686 1.894.694-3.957a.565.565 0 0 0-.163-.505L1.71 6.745l4.052-.576a.525.525 0 0 0 .393-.288L8 2.223l1.847 3.658a.525.525 0 0 0 .393.288l4.052.575-2.906 2.77a.565.565 0 0 0-.163.506l.694 3.957-3.686-1.894a.503.503 0 0 0-.461 0z"/>
                </svg>`,
          title: 'Owner Yang Tamvan',
          body: 'Owner fynjoki itu tampan banget dah suer. Jangankan cewe, kepala sekolah bentak Nayla gua buakar sekolahnya. Eh wait salah teks. Dahlah gpp pokoknya gitu.'
        }
      ]
    }
  }
}
</script>

<template>
  <div id="Kenapa">
    <div class="left">
      <div class="title">
        <h2 title="Gajelas hadeh">Kenapa Sih Lu Harus Banget Dengan Sangat Amat Harus Pake Layanan Joki FynJoki?</h2>
      </div>
      <div class="desc">
        <div>
          Gak ada kelebihannya sih, kadang kami juga males buat ngejoki tapi ya gimana namanya butuh duit. 
          Tapi gak juga sih ada beberapa kelebihan dari layanan joki kami yang bisa lu iqro (baca).
        </div>
      </div>
      <div class="data">
        <div>
          <p>Jumlah Pengguna</p>
          <p>1.000.069</p>
        </div>
        <div>
          <p>Persentase Kepuasan</p>
          <p>169%</p>
        </div>
      </div>
    </div>
    <div class="right">
      <div class="kelebihanKelebihan">
        <Kelebihan v-for="lebih in kelebihan" :kelebihan="lebih"/>
      </div>
    </div>
  </div>
</template>

<style scoped>
#Kenapa {
  padding: 20px 35px;
  margin-top: 110px;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}

#Kenapa .left {
  width: 30%;
}

#Kenapa .left .title {
  font-family: 'Dosis', sans-serif;
  font-weight: bolder;
  font-size: 1.2em;
}

#Kenapa .left .desc {
  margin: 25px 0 30px;
  font: normal bold 1.1em/25px 'Quicksand', sans-serif;
  color: #555151;
}

#Kenapa .left .data {
  display: flex;
  font-weight: bold;
  font-size: 1.1em;
  justify-content: space-between;
}

#Kenapa .left .data div {
  text-align: center;
}

#Kenapa .left .data div p:first-child {
  color: #555151;
  margin-bottom: 8px;
}

#Kenapa .left .data div:first-child {
  border-right: 1px solid #000000;
  padding-right: 25px;
}

#Kenapa .right {
  width: 65%;
}

#Kenapa .right .kelebihanKelebihan {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  padding: 0 0px;
}

@media (max-width: 1150px) {
  #Kenapa .left {
    width: 40%;
  }
  #Kenapa .right {
    width: 50%;
  }
}

@media (max-width: 950px) {
  #Kenapa {
    padding: 20px;
    margin-top: 40px;
  }

  #Kenapa .left {
    width: 100%;
    text-align: center;
  }

  #Kenapa .right {
    width: 100%;
    margin-top: 60px;
  }

  #Kenapa .left .data {
    display: flex;
    font-weight: bold;
    font-size: 1.1em;
    justify-content: center;
  }

  #Kenapa .left .data div:last-child {
    padding-left: 25px;
  }

  #Kenapa .left .desc {
    margin: 40px 0;
  }
}

@media (max-width: 425px) {
  #Kenapa .left .data div p:first-child {
    font-size: .9em;
    margin-bottom: 5px;
  }

  #Kenapa .left .data div p:last-child {
    font-size: .9em;
  }
}

@media (max-width: 375px) {
  #Kenapa .left .data div p:first-child {
    font-size: .8em;
  }

  #Kenapa .left .data div p:last-child {
    font-size: .9em;
  }
}
</style>