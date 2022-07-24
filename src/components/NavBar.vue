<script>
export default {
  props: {
    activenav: {
      type: String,
      default: 'beranda'
    },
    scrolled: {
      type: Boolean,
      default: window.scrollY > 0
    }
  },
  data() {
    return {
      toggled: false
    }
  }
}
</script>

<template>
  <div :class="scrolled || toggled ? 'navbar scrolled' : 'navbar'">
    <div class="navbar-brand">
      <h3>FYNJOKI</h3>
    </div>
    <nav :class="toggled ? 'toggled' : ''">
      <ul>
        <li :class="activenav === 'beranda' ? 'active' : ''">
          <a href="#Beranda">Beranda</a>
        </li>
        <li :class="activenav === 'kenapa' ? 'active' : ''">
          <a href="#Kenapa">Kenapa Fynjoki</a>
        </li>
        <li :class="activenav === 'harga' ? 'active' : ''">
          <a href="#Harga">Harga</a>
        </li>
        <li :class="activenav === 'testimoni' ? 'active' : ''">
          <a href="#Testimoni">Tetimoni</a>
        </li>
        <li>
          <a href="#">Joki Sekarang →</a>
        </li>
      </ul>
    </nav>
    <div class="navbar-toggler">
      <input type="checkbox" name="navbarToggler" id="navbarToggler"  @input="toggled = $event.target.checked">
      <span></span>
      <span></span>
      <span></span>
    </div>
  </div>
</template>

<style>
.navbar {
  display: flex;
  padding: 10px 30px;
  justify-content: space-between;
  position: fixed;
  right: 0;
  left: 0;
  top: 0;
  align-items: center;
  transition: .3s;
  z-index: 1;
}

.navbar.scrolled {
  padding: 15px 45px;
  box-shadow: 1px 1px 5px rgba(0,0,0,.3);
  background-color: #ffffff;
}

.navbar nav {
  width: 45%;
}

.navbar .navbar-toggler {
  display: none;
  position: relative;
}

.navbar .navbar-toggler span {
  display: block;
  background-color: #000;
  height: 2px;
  width: 25px;
  border-radius: 3px;
  transition: .3s;
}

.navbar .navbar-toggler input {
  position: absolute;
  transform: scale(150%);
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  opacity: 0;
  z-index: 3;
}

.navbar .navbar-toggler span:nth-child(2), .navbar .navbar-toggler span:last-child  {
  transform-origin: 0;
}

.navbar .navbar-toggler input:checked ~ span:nth-child(2) {
  transform: rotate(43deg) translateY(1px) translateX(.9px);
}

.navbar .navbar-toggler input:checked ~ span:nth-child(3) {
  transform: scale(0);
}

.navbar .navbar-toggler input:checked ~ span:last-child {
  transform: rotate(-43deg) translateY(1.5px) translateX(-1.5px);
}

.navbar .navbar-toggler span:nth-child(2), .navbar .navbar-toggler span:nth-child(3)  {
  margin-bottom: 6px;
}

.navbar nav ul {
  align-items: center;
  width: 100%;
  display: flex;
  justify-content: space-between;
}

.navbar nav ul li a {
  color: rgb(124, 124, 124);
  font-weight: 500;
  transition: .3s;
}

.navbar nav ul li a:hover {
  color: rgb(58, 58, 58);
}

.navbar nav ul li.active a {
  color: #000000;
}

.navbar nav ul li:last-child a {
  background-color: rgb(96, 44, 163);
  color: #ffffff;
  padding: 8px 15px;
  border-radius: 5px;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: .9em;
}

.navbar nav ul li:last-child a:hover {
  background-color: rgb(63, 28, 109);
  color: #eaeaea;
}

/* Reponsive */
@media (max-width: 1190px) {
  .navbar nav {
    width: 60%;
  }
}

@media (max-width: 900px) {
  .navbar {
    padding: 10px 20px;
  }
  
  .navbar.scrolled {
    padding: 15px 25px;
  }

  .navbar nav {
    transition: .3s;
    position: absolute;
    padding: 20px 15px;
    top: 58px;
    height: 1000px;
    width: 100%;
    right: -100%;
    background-color: #ffffff;
    transition-delay: .5s;
  }

  .navbar nav.toggled {
    box-shadow: 1px 1px 5px rgba(0,0,0,.3);
    border-radius: 3px;
    right: -20%;
    transition-delay: 0s;
  }
  
  .navbar nav ul {
    display: block;
  }

  .navbar nav a {
    display: block;
    transition-delay: .0s;
  }

  .navbar nav ul li:last-child a {
    background-color: inherit;    
    padding: 0;
    border-radius: 0;
    color: rgb(145, 145, 145);
    font-size: 1em;
    display: inline;
  } 

  .navbar nav.toggled li a {
    border-bottom: 2px solid rgb(145, 145, 145);
    margin-bottom: 25px;
    transition-delay: .5s;
  }

  .navbar nav li:last-child a {
    border-bottom: none;
  }

  .navbar nav.toggled li:last-child a {
    background-color: rgb(96, 44, 163);
    color: #ffffff;
    padding: 8px 15px;
    border-radius: 5px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: .9em;
  }

  .navbar nav.toggled li.active a {
    border-bottom: 2px solid #000000;
  }

  .navbar nav li:last-child a {
    width: fit-content;
  }

  .navbar .navbar-toggler {
    display: block;
  }
}
</style>