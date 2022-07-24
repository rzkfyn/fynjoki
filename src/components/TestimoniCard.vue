<script>
export default {
  props: {
    testimoni: {
      type: Object,
      default: {}
    }
  },
  data() {
    return {
      star: `<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-star-fill" viewBox="0 0 16 16">
                <path d="M3.612 15.443c-.386.198-.824-.149-.746-.592l.83-4.73L.173 6.765c-.329-.314-.158-.888.283-.95l4.898-.696L7.538.792c.197-.39.73-.39.927 0l2.184 4.327 4.898.696c.441.062.612.636.282.95l-3.522 3.356.83 4.73c.078.443-.36.79-.746.592L8 13.187l-4.389 2.256z"/>
              </svg>`,
      goldenStar: `<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-star-fill gold" viewBox="0 0 16 16">
                    <path d="M3.612 15.443c-.386.198-.824-.149-.746-.592l.83-4.73L.173 6.765c-.329-.314-.158-.888.283-.95l4.898-.696L7.538.792c.197-.39.73-.39.927 0l2.184 4.327 4.898.696c.441.062.612.636.282.95l-3.522 3.356.83 4.73c.078.443-.36.79-.746.592L8 13.187l-4.389 2.256z"/>
                  </svg>`
    }
  },
  methods: {
    rate(stars) {
      let res = '';
      for (let i = 1; i <= 5; i++){
        if (i <= stars) {
          res += this.goldenStar;
        } else {
          res += this.star;
        }
      }
      return res;
    }
  }
}
</script>

<template>
  <div class="TestimoniCard">
    <div class="header">
      <div class="photo">
        <img :src="`/imgs/${testimoni.img}`" :alt="testimoni.nama">
      </div>
      <div class="userdata">
        <p class="username">{{ testimoni.name }}</p>
        <p class="occupation">{{ testimoni.occupation }}</p>
      </div>
    </div>
    <div class="body">
      <p>
        {{ testimoni.feedback }}
      </p>
    </div>
    <div class="footer" v-html="rate(testimoni.rating)">
    </div>
  </div>
</template>

<style>
.TestimoniCard {
  background-color: #ffffff;
  border-radius: 8px;
  max-width: 350px;
  width: 100%;
  margin-top: 40px;
  box-shadow: 1px 1px 5px rgba(0,0,0,.2);
  transition: .3s;
  user-select: none;
}

.TestimoniCard:hover {
  transform: translateY(-10px);
}

.TestimoniCard .header { padding: 10px 15px }
.TestimoniCard .body { padding: 0 15px }
.TestimoniCard .footer { padding: 15px }

.TestimoniCard .header {
  display: flex;
  align-items: center;
  background-color: #fdfdfd;
  border-top-left-radius: 8px;
  border-top-right-radius: 8px;
  border-bottom: 1px solid #c9c9c9;
}

.TestimoniCard .header .photo {
  width: 45px;
  height: 45px;
  margin-right: 10px;
  box-shadow: 1px 1px 2px rgba(0,0,0,.2);
  border-radius: 4px;
}

.TestimoniCard .header .photo img {
  width: 100%;
  height: 100%;
  border-radius: 4px;
}

.TestimoniCard .header .userdata  {
  font-size: .9em;
}

.TestimoniCard .header .userdata p:first-child {
  font-weight: bolder;
}


.TestimoniCard .body {
  margin-top: 10px;
}

.TestimoniCard .footer .bi-star-fill {
  margin-right: 5px;
  color: rgb(110, 110, 110);
  cursor: pointer;
  transition: .2s;
}

.TestimoniCard .footer .bi-star-fill:hover {
  transform: scale(150%);
}

.TestimoniCard .footer .bi-star-fill.gold {
  color: rgb(224, 209, 71);
}
</style>