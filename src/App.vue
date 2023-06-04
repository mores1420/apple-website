<template>
  <div class="main">
    <transition name="fade">
    <!-- 导航栏 -->
      <img v-if="showImage" class="fullscreen-image" src="../public/data/OPENPIC.jpg" alt="Animated Image">
    </transition>
    <button @click="begin" class="rounded-button">BEGIN</button>
  </div>
</template>

<script>
import openPic from "@/assets/OPENPIC.jpg";

export default {
  data() {
    return {
      showImage: false,
      openIMG: true,
      openPic: openPic
    };
  },
  mounted(){
    setTimeout(() => {
      this.showImage=true;
    }, 500);
  },
  /*
  components:{
    Header
  }
  */
};
</script>

<style>
/* 添加样式来美化页面 */
#app {
  text-align: center;
  padding: 20px;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  padding: 0;
}

nav li {
  margin-right: 10px;
}

nav a {
  text-decoration: none;
  color: rgb(54, 114, 54);
}

main {
  margin-top: 20px;
}

button {
  margin-top: 10px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%,-50%);
  font-size: 24px;
  padding: 12px 24px;
}

.fullscreen-image {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.rounded-button{
  border: none;
  border-radius: 50%;
  padding: 12px 24px;
  font-size: 24px;
  background-color: #007bff;
  color: #fff;
  cursor: pointer;
  transition: background-color 0.3s;
}

.rounded-button:hover {
  background-color: #0056b3;
}

</style>

