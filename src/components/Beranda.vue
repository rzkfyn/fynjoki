<template>
  <div id="Beranda">
    <div class="desc">
      <div class="title">
        <h2>Solusi Buat Lu Lu Pada</h2>
        <h2>Yang Capek Dapet Error Di Tugas Pemrograman</h2>
      </div>
      <div>
        <p>
          Cape karena tugas coding banyak mulu udah gitu pas ngerjain, errornya udah kaya sebanyak dosa lu? Udah ngerjainnya susah tambah error mulu itu pastinya bikin gak mood. Dengan layanan ini lu gak usah mikirin lagi tugas coding yang susah!
        </p>
      </div>
      <div class="btns">
        <a href="#">Pelajari Selengkapnya</a>
        <a href="#">Coba Sekarang</a>
      </div>
    </div>
    <div class="ilust">
      <img src="/imgs/code.jpg" alt="ilustrasi">
    </div>
  </div>
</template>

<style>
#Beranda {
  margin-top: 50px;
  display: flex;
  padding: 20px 40px;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
}

#Beranda div.desc {
  width: 55%;
}

#Beranda div.ilust {
  width: 45%;
}

#Beranda div.desc .title {
  padding-right: 20px;
  font-weight: bolder;
  font-family: 'Dosis', sans-serif;
  font-size: 1.2em;
  color: rgb(46, 45, 45);
}

#Beranda div.desc div:nth-child(2) {
  padding: 15px 0;
}

#Beranda div.desc div:nth-child(2) p {
  font: normal normal 1.1em/28px 'Quicksand', sans-serif;
  color: rgb(78, 78, 78);
  font-weight: bold;
}

#Beranda div.desc div.btns {  
  display: flex;
  justify-content: flex-start;
  margin-top: 10px;
}

#Beranda div.desc div.btns a {
  padding: 8px 15px;
  color: #eaeaea;
  background-color: rgb(123, 46, 196);
  border-radius: 2.5px;
  font-weight: bold;
  text-align: center;
  transition: .3s;
  display: inline-block;
}

#Beranda div.desc div.btns a:hover {
  transform: translateY(-3px);
}

#Beranda div.desc div.btns a:last-child{
  color: rgb(116, 54, 173);
  background-color: rgba(134, 76, 189, .2);
  border: 1px solid rgb(134, 76, 189);
  margin-left: 20px;
}

#Beranda div.ilust {
  text-align: end;
}

#Beranda div.ilust img {
  width: 90%;
}

/* Responsive */

@media (max-width: 950px) {
  #Beranda div.desc, #Beranda div.ilust {
    width: 100%;
  }
  
  #Beranda div.ilust {
    text-align: center;
  }

  #Beranda div.ilust img {
    width: 90%;
  }

  #Beranda div.desc div:nth-child(2) {
    margin: 20px 0;
  }

  #Beranda div.ilust {
    margin-top: 40px;
  }
}

@media (max-width: 500px) {
  #Beranda {
    padding: 20px;
  }
  
  #Beranda div.desc div.btns {
    width: 100%;
    flex-wrap: wrap;
  }

  #Beranda div.desc div.btns a {
    display: block;
    width: 100%;
    margin: 8px auto;
  }

  #Beranda div.desc div.btns a:last-child {
    margin-left: 0;
  }
}
</style>