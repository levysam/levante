<template>
 <div>
  <Navbar></Navbar>
  <b-img :src="userImgSrc" class="img-fluid w-100"></b-img>
  <div class="margin col-12 d-flex flex-column align-items-left">
    <h3 class="text-white">{{username}}</h3>
    <p class="text-white mt-3">{{userProfession}}</p>
    <SocialArea :likes="likes" :following="following" :followers="followers"></SocialArea>
  </div>
  </div>
</template>

<style scoped>
  .margin {
    margin-top: -12rem;
  }
</style>

<script>
import Navbar from '../components/Navbar'
import SocialArea from '../components/SocialArea'

export default {
  name: 'Login',
  components: {
    Navbar,
    SocialArea
  },
  data: function () {
    return {
    username: 'TesteUsername',
    userImgSrc: '/assets/profile.jpg',
    userProfession: 'Frontend Developer',
    likes: 1000,
    following: 20,
    followers: 100
    }
  }
}
</script>
