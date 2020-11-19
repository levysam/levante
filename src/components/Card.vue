<template>
    <div>
      <b-img :src="imgPath"></b-img>
      <p>{{title}}</p>
    </div>
</template>

<script>

export default {
  name: 'Card',
  components: {
  },
  props: {
        title: String,
        imgPath: String
      }
}
</script>