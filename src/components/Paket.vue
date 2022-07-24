<script>
export default {
  props: {
    paket: {
      type: Object,
      default: {}
    }
  }
}
</script>

<template>
  <div class="Paket">
    <div class="header">
      <div class="title">
        <h2>{{ paket.title }}</h2>
      </div>
      <div class="price">
        <h3>{{ paket.price }}</h3>
      </div>
      <div class="desc">
        <p>
          {{ paket.desc }}
        </p>
      </div>
    </div>
    <div class="body">
      <ul>
        <li v-for="untung in paket.keuntungan">
          <span>
            <img src="/imgs/check.svg" alt="check">
          </span>
          <span>
            {{ untung }}
          </span>
        </li>
      </ul>
    </div>
    <div class="footer">
      <a href="#">
        Pilih Paket Ini
      </a>
    </div>
  </div>
</template>

<style scoped>
.Paket {
  padding: 50px 0;
  text-align: left;
  border-radius: 8px;
  background-color: #ffffff;
  width: 100%;
  max-width: 350px;
  margin-bottom: 30px;
  border: 1px solid transparent;
  transition: .3s;
}

.Paket:hover {
  transform: translateY(-5px);
  border: 1px solid rgb(223, 158, 240);
}

.Paket .title, .price, .desc, .body {
  padding: 0 35px;
  margin-bottom: 25px;
}

.Paket .title h2 {
  font-size: 1.2em;
  color: #5f5f5f;
  font-weight: 600;
}

.Paket .price {
  font-size: 1.4em;
}

.Paket .desc {
  font-size: 1.1em;
  color: #525252be;
}

.Paket .body {
  margin-top: 30px;
}

.Paket .body ul li {
  display: flex;
  margin-bottom: 22px;
  font-weight: bolder;
  font-size: 1.1em;
  align-items: center;
}

.Paket .body ul li span:first-child {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 25px;
  height: 25px;
  padding: 2px;
  background-color: rgba(129, 129, 129, 0.1);
  border-radius: 50%;
}

.Paket .body ul li span:first-child img {
  width: 80%;
}

.Paket .body ul li span:last-child {
  margin-left: 5px;
}

.Paket .footer {
  margin-top: 40px;
  padding: 0 20px;
}

.Paket .footer a {
  padding: 8px 0;
  text-align: center;
  display: block;
  color: #ffffff;
  background-color: rgb(105, 49, 158);
  border-radius: 3px;
  font-weight: bolder;
  transition: .3s;
}

.Paket .footer a:hover {
  color: #dddddd;
}
</style>