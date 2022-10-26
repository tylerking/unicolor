<!--
Unicolor: A dark theme inspired by unicorns
-->
<template>
  <div class="unicolor">
    <h1>{{ title }}</h1>
    <p>{{ description }}</p>
    <ul>
      <li v-for="(color, index) in colors" v-bind:key="index">{{ color }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Unicolor',
  data: function () {
    return {
      title: 'Unicolor',
      description: 'A dark theme inspired by unicorns',
      color: null,
      colors: ['Pink','Blue','Purple']
    }
  },
  methods: {
    randomColor () {
      this.color = true
    }
  }
}
</script>

<style lang="scss" scoped>
$pink: #F4869E;
.unicolor {
  background: $pink;
  h1 {
    size: 24px;
  }
}
</style>