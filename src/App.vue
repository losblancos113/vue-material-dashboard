<template lang="pug">
#app
  .wrapper
    sidebar
    .main-panel
      navigation
      router-view
      md-footer
</template>

<script>
import Navigation from '@/components/Navigation'
import MdFooter from '@/components/Footer'
import Sidebar from '@/components/Sidebar'

export default {
  name: 'app',
  components: {
    Navigation,
    MdFooter,
    Sidebar
  },

  mounted() {
    this.initMaterial()
  },

  updated() {
    this.initMaterial()
  },

  methods: {
    initMaterial() {
      $.material.init() // eslint-disable-line
    }
  }
}
</script>

<style lang="scss">
@import "./assets/sass/md/_variables.scss";

.table {
  thead {
    th {
      font-weight: $headings-font-weight;
    }
  }
}

@media (min-width: 992px) {
  .typo-line {
    padding-left: 140px;
    margin-bottom: 40px;
    position: relative;
    .category {
      transform: translateY(-50%);
      top: 50%;
      left: 0px;
      position: absolute;
    }
  }
}

.places-buttons .btn {
  margin-bottom: 30px
}

.space-70 {
  height: 70px;
  display: block;
}

.sidebar .nav>li.active-pro {
  position: absolute;
  width: 100%;
  bottom: 10px;
}

.tim-row {
  margin-bottom: 20px;
  padding-top: 50px;
  h3 {
    margin-top: 0;
  }
}

.tim-typo {
  padding-left: 25%;
  margin-bottom: 40px;
  position: relative;
  .tim-note {
    bottom: 10px;
    color: #c0c1c2;
    display: block;
    font-weight: 400;
    font-size: 13px;
    line-height: 13px;
    left: 0;
    margin-left: 20px;
    position: absolute;
    width: 260px;
  }
}
</style>

