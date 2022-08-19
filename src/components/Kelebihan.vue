<script>
export default {
  props: {
    kelebihan: {
      type: Object,
      default: {}
    }
  }
}
</script>

<template>
  <div class="kelebihan">
    <div class="header">
      <div class="icon" v-html="kelebihan.icon">
      </div>
      <div class="title">
        <h4>{{ kelebihan.title }}</h4>
      </div>
    </div>
    <div class="body" v-html="kelebihan.body">
    </div>
  </div>
</template>

<style>
.kelebihan {
  width: 45%;
  padding: 20px;
  border-radius: 5px;
  background-color: rgba(131, 86, 190, 0.3);
  margin-bottom: 25px;
  user-select: none;
  transition: .3s;
  border: 2px solid rgba(0, 0, 0, 0);
}

.kelebihan:hover {
  transform: translateY(-10px);
  border: 2px solid rgba(131, 86, 190, 1);
  justify-items: auto;
}

.kelebihan .header {
  display: flex;
  align-items: center;
  margin-bottom: 10px;
}

.kelebihan .header .icon {
  padding: 8px;
  background-color: rgba(131, 86, 190, 0.3);
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 2.5px;
  margin-right: 10px;
  color: rgb(98, 39, 177);
}

.kelebihan .body {
  color: rgb(102, 102, 102);
}

/* Responsive */
@media (max-width: 1150px) {
  .kelebihan {
    width: 100%;
  }
}
</style>