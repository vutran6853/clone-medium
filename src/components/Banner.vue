<template>
  <div class="container">
    <div class="flex-item-a">
      <h3>{{ banner.title }}</h3>
      <p>{{ banner.message }}</p>
    </div>
    <div class="flex-item-b">
      <input placeholder="Enter Email..." type="email">
      <button>Sigin up</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Banner',
  props: {
    banner: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  height: 250px;
  width: 75%;
  justify-content: space-evenly;
  align-items: center;
  background-color: lightgray;
  margin: auto;
  margin-top: 5rem;
  margin-bottom: 5rem;
}

.flex-item-a {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  height: 100px;
}

.flex-item-a > h3 {
  font-size: 2.5rem;
}

.flex-item-a > p {
  font-size: 1.5rem
}

.flex-item-b > input {
  width: 30rem;
  height: 2rem;
  background: none;
  border-style: none;
  border-bottom: 1px solid lightcoral;
  outline: none;
  cursor: text;
}

.flex-item-b > input::placeholder {
  color: lightcoral;
}

.flex-item-b > button {
  height: 2rem;
  width: 5rem;
  background-color: black;
  border-style: none;
  color: white;
}

.flex-item-b > button:hover {
  background-color: gray;
  cursor: pointer;
}
</style>
