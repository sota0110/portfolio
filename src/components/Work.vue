<template>
  <a :href="urlname" class="container">
    <img :src="imgname" alt="">
    <h3>{{ titlename }}</h3>
    <p>{{ username }}</p>
  </a>
</template>

<script>
export default {
  name: 'Work-contents',
  props:{
    titlename: String,
    username: String,
    urlname: String,
    imgname: String
  }
}
</script>