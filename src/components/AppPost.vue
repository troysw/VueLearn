<template>
  <div>
    <div class="post-header">
      <div class="profile"></div>
      <span class="profile-name">{{AppData.name}}</span>
    </div>
    <div class="post-body" :style="{backgroundImage : `url(${AppData.postImage})`}"></div>
    <div class="post-content">
      <p>{{AppData.likes}} Likes</p>
      <p><strong>{{AppData.name}}</strong> {{AppData.content}}</p>
      <p class="date">{{AppData.date}}</p>
    </div>
</div> 
</template>

<script>
export default {
name: 'AppContainer',
props : {
  AppData : Array,
  },
}
</script>

<style>
.post {
  width: 100%;
}
.profile {
  background-image: url("https://placeimg.com/100/100/arch");
  width: 30px;
  height: 30px;
  background-size: 100%;
  border-radius: 50%;
  float: left;
}
.profile-name {
  display: block;
  float: left;
  padding-left: 10px;
  padding-top: 7px;
  font-size: 14px;
}
.post-header {
  height: 30px;
  padding: 10px;
}
.post-body {
  background-image: url("https://placeimg.com/640/480/animals");
  height: 450px;
  background-position: center;
  background-size: cover;
}
.post-content {
  padding-left: 15px;
  padding-right: 15px;
  font-size: 14px;
}
.date {
  font-size: 11px;
  color: grey;
  margin-top: -8px;
} 
</style>