<template>
<div class="d-flex">
    <div class="col-1"></div>
    <div class="d-flex col-10 justify-content-around bg-danger rounded px-3 py-3">
        <div class="text-white"><p>Likes</p><p>{{likes}}</p></div>
        <div class="text-white"><p>Following</p><p>{{following}}</p></div>
        <div class="text-white"><p>Followers</p><p>{{followers}}</p></div>
        </div>
    <div class="col-1"></div>
</div>
</template>

<script>
  export default {
    name: 'SocialArea',
    props: {
        likes : Number,
        following: Number,
        followers: Number
      }
  }
</script>
