<template>
 <div>
  <SideMenu page="Profile"></SideMenu>
  <b-img :src="userImgSrc" class="img-fluid w-100"></b-img>
  <div class="margin col-12 d-flex flex-column align-items-left">
    <h3 class="text-white">{{username}}</h3>
    <p class="text-white mt-3">{{userProfession}}</p>
    <SocialArea :likes="likes" :following="following" :followers="followers"></SocialArea>
  </div>
    <div class="d-flex">
      <div v-for="example in ExampleList" :key="example.id" class="col-6 col-md-4 col-lg-3 d-flex flex-column justify-content-center align-items-left">
        <b-img :src="example.path" class="img-fluid"></b-img>
        <div class="d-flex flex-column align-items-left pl-3"><p>{{example.title}}</p>
        <p>{{example.type}}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
  .margin {
    margin-top: -12rem;
  }
</style>

<script>
import SideMenu from '../components/SideMenu'
import SocialArea from '../components/SocialArea'
export default {
  name: 'Login',
  components: {
    SideMenu,
    SocialArea
  },
  data: function () {
    return {
    username: 'TesteUsername',
    userImgSrc: '/assets/profile.jpg',
    userProfession: 'Frontend Developer',
    likes: 1000,
    following: 20,
    followers: 100,
    ExampleList : [
      {
        id: 1,
        title: "testeste",
        path: "/assets/post.jpg",
        type: "Adventure"
      },
      {
        id: 2,
        title: "testeste2",
        path: "assets/post.jpg",
        type: "travel"
      }
    ]
    }
  }
}
</script>
