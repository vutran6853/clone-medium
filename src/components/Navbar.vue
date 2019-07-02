<template>
  <div class="container">
    <div class="top-navbarItem">
      <h3>Medium</h3>
      <span>
        <img src="../../src/assets/search.png" alt="broken">
        <p>Become a Member</p>
        <p>Sign in</p>
        <button>Get started</button>
      </span>
    </div>
    <div class="botton-navbarItem">
      <p v-for="(value, index) in navbarItem" v-bind:key="index">
        {{ value }}
      </p>
    </div>
  </div>
</template>

<script>
// import { Component, Prop, Vue } from 'vue-property-decorator'

export default {
  name: 'Navbar',
  props: {
    navbarItem: Array,
    required: true
  }
}
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  width: 75%;
  margin: auto;
}

.top-navbarItem {
  /* background-color: blue; */
  color: black;
  display: flex;
  height: 4rem;
  align-items: center;
  justify-content: space-between;
}

.top-navbarItem > span {
  display: grid;
  grid-template-columns: 40px 140px 60px 100px;
}

.top-navbarItem > span > p {
  align-self: center;
}

.top-navbarItem > span > img {
  height: 20px;
  width: 20px;
  align-self: center;
}

.top-navbarItem > span > button {
  border-style: none;
  height: 2rem;
  background-color: white;
  border: 1px solid red;
  border-radius: 4px;
}

.top-navbarItem > span > button:hover {
  background-color: cadetblue;
}

.botton-navbarItem {
  /* background-color: yellow; */
  display: flex;
  justify-content: space-between;
}

</style>
