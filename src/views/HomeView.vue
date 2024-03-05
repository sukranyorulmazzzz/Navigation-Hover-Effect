<template>
  <div class="home">
    <h1 class="text t1">Popular Series <span>Popular Series</span></h1>
    <h1 class="text t2">New Releases <span>New Releases</span></h1>
    <h1 class="text t3">Recommendations <span>Recommendations</span></h1>
    <h1 class="text t4">Japanese Culture <span>Japanese Culture</span></h1>
    <h1 class="text t5">Anime News <span>Anime News</span></h1>
    <div class="images">
      <img id="i1" src="../assets/image1.png" alt="" />
      <img id="i2" src="../assets/image2.png" alt="" />
      <img id="i3" src="../assets/image3.png" alt="" />
      <img id="i4" src="../assets/image4.png" alt="" />
      <img id="i5" src="../assets/image5.png" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeView",
  components: {},
};
</script>

<style scoped>
.home {
  width: 100%;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.text {
  font-size: 8vw;
  position: relative;
  margin: 0;
  display: flex;
  cursor: pointer;
  border-bottom: 1px solid #555;
  line-height: 120%;
}
.home .text:first-child {
  border-top: 1px solid #555;
}
.text span {
  position: absolute;
  width: 100%;
  height: 100%;
  background-color: #4345cf;
  color: black;
  clip-path: polygon(0 50%, 100% 50%, 100% 50%, 0 50%);
  transition: clip-path 0.3s ease;
}
.text:hover span {
  clip-path: polygon(0% 0%, 100% 0%, 100% 100%, 0% 100%);
}
.images {
  width: 30vw;
  height: 60vh;
  display: flex;
  justify-content: center;
  align-items: center;
  position: absolute;
  right: 5%;
  top: 50%;
  transform: translateY(-50%);
}
.images img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  position: absolute;
  opacity: 0;
  transition: opacity 0.3s ease;

  border-radius: 0.75rem;
}
.t1:hover ~ .images #i1,
.t2:hover ~ .images #i2,
.t3:hover ~ .images #i3,
.t4:hover ~ .images #i4,
.t5:hover ~ .images #i5 {
  opacity: 1;
  transform: translateY(0%);
}
</style>
