<template>



<div class="parent-container">

<div class="title-head">
    <h1>SELECT YOUR MEAL</h1>
  </div>

  <div class="menu">

    <div class="section1 section-title"> <h1>Fruits</h1>
      <div><input type="radio" value="Banana" v-model="selectedOption1" />
        <img src="assets/banana.png" alt=""></div>
      <div><input type="radio" value="Strawberry" v-model="selectedOption1" />
        <img src="assets/strawb.png" alt=""></div>
      <div><input type="radio" value="Mango" v-model="selectedOption1" />
        <img src="assets/mango.png" alt=""></div>
  </div>

    <div class="sectinon2 section-title"> <h1>Vegetables</h1>
      <div><input type="radio" value="Letuce" v-model="selectedOption2" />
        <img src="assets/leaf.png" alt=""></div>
      <div><input type="radio" value="Eggplant" v-model="selectedOption2" />
        <img src="assets/eggplant.png" alt=""></div>
      <div><input type="radio" value="Tomato" v-model="selectedOption2" />
        <img src="assets/tomato.png" alt=""></div>
    </div>

    <div class="sectinon3 section-title"> <h1>Grains</h1>
      <div><input type="radio" value="Oats" v-model="selectedOption3" />
        <img src="assets/oats.png" alt=""></div>
      <div><input type="radio" value="Wheat" v-model="selectedOption3" />
        <img src="assets/wheat.png" alt=""></div>
      <div><input type="radio" value="Corn" v-model="selectedOption3" />
        <img src="assets/corn.png" alt=""></div>
    </div>

    <div class="sectinon4 section-title"> <h1>Protiens</h1>
      <div><input type="radio" value="Meat" v-model="selectedOption4" />
        <img src="assets/meat.png" alt=""></div>
      <div><input type="radio" value="Fish" v-model="selectedOption4" />
        <img src="assets/fish1.png" alt=""></div>
      <div><input type="radio" value="Tofu" v-model="selectedOption4" />
        <img src="assets/tofu.png" alt=""></div>
    </div>

  </div>

  <div class="selected">
    <div><p>Selected option: {{ selectedOption1 }}</p>
         <img :src="getImage(selectedOption1)"  />
    </div>
    <div><p>Selected option: {{ selectedOption2 }}</p>
      <img :src="getImage(selectedOption2)" />
    </div>
    <div><p>Selected option: {{ selectedOption3 }}</p>
      <img :src="getImage(selectedOption3)" />
    </div>
    <div><p>Selected option: {{ selectedOption4 }}</p>
      <img :src="getImage(selectedOption4)" />
    </div>
  </div>

</div>

  
</template>

<script>
export default {
  data() {
    return {
      selectedOption1: " ",
      selectedOption2: " ",
      selectedOption3: " ",
      selectedOption4: " "


    };
  },

   methods: {
    getImage(optionValue) {
      // Define a mapping of option values to image URLs
      const imageMappings = {
        Banana: "assets/banana.png",
        Strawberry: "assets/strawb.png",
        Mango: "assets/mango.png",
        Lettuce: "assets/leaf.png",
        Eggplant: "assets/eggplant.png",
        Tomato: "assets/tomato.png",
        Oats: "assets/oats.png",
        Wheat: "assets/wheat.png",
        Corn: "assets/corn.png",
        Meat: "assets/meat.png",
        Fish: "assets/fish1.png",
        Tofu: "assets/tofu.png",
      };

      // Return the image URL based on the selected option value
      return imageMappings[optionValue] || "";
    },
  },
  
};
</script>

<style scoped>
  @import 'style.css';
</style>





