<template>
  <div class="app" :class="mode">
    <TheHeader :mode="mode" @toggle="toggle"/>
    <TheContent :mode="mode"/>
  </div>
</template>

<script>
import TheHeader from "@/components/TheHeader";
import TheContent from "@/components/TheContent";
export default {
  name: "app",
  components: { TheHeader, TheContent },
  data() {
    return {
      mode: "dark"
    };
  },
  created() {
    window.addEventListener("keyup", this.keyPress);
  },
  methods: {
    keyPress(e) {
      if (e.key === "t") {
        this.toggle();
      }
    },

    toggle() {
      if (this.mode === "dark") {
        this.mode = "light";
      } else {
        this.mode = "dark";
      }
    }
  }
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Roboto", sans-serif;
}
.app {
  width: 100vw;
  min-height: 100vh;
  background: #f3f3f3;
  color: #152028;
  transition: background 0.6s ease-in-out;
}

.dark {
  background: #192734;
  color: #fefefe;
}
</style>
