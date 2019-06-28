<template>
  <div class="content">
    <h3>This is {{mode}} mode</h3>
    <div class="image-grid">
      <div class="col">
        <img src="https://source.unsplash.com/random/1600x900">
      </div>
      <div class="col">
        <img src="https://source.unsplash.com/1600x900">
      </div>
      <div class="col">
        <img src="https://source.unsplash.com/featured/1600x900">
      </div>
    </div>
    <p
      class="para"
    >Lorem ipsum dolor sit amet consectetur adipisicing elit. Adipisci ut, quasi eos error perspiciatis laudantium consectetur officiis? Obcaecati libero officia quas atque dolorem cupiditate repellat ut dicta ratione iusto sequi porro quos recusandae ipsam, eligendi perferendis, laborum eum expedita quo maiores tempore, doloribus saepe. Eligendi nesciunt animi delectus vitae eius?</p>
  </div>
</template>

<script>
export default {
  props: ["mode"]
};
</script>

<style>
.content {
  padding: 25px;
}

.content h3 {
  font-size: 28px;
  text-transform: uppercase;
  font-weight: 300;
  margin-bottom: 25px;
}
.image-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 15px;
}

.image-grid .col img {
  width: 100%;
  height: auto;
  border-radius: 10px;
}

.para {
  width: 100%;
  max-width: 600px;
  margin: 25px auto 0px;
}
</style>
