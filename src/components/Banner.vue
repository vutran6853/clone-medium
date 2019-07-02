// This Wil Def As Functional Components
<template functional>
  <div class="container">
    <div class="flex-item-a">
      <h3>{{ props.banner.title }}</h3>
      <p>{{ props.banner.message }}</p>
    </div>
    <div class="flex-item-b">
      <input placeholder="Enter Email..." type="email">
      <button>Sigin up</button>
    </div>
  </div>
</template>``

<script>
export default {
  name: 'Banner'
}
</script>

<style scoped>

.container {
  background-color: lightgray;
  margin: 5rem;
  display: flex;
  flex-direction: column;
  height: 250px;
  justify-content: space-evenly;
  align-items: center;
}

.flex-item-a {
  /* background-color: red; */
  align-items: center;
  display: flex;
  flex-direction: column;
  height: 100px;
  justify-content: space-around;
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
}

.flex-item-b > input::placeholder {
  color: lightcoral;
}

.flex-item-b > button {
  height: 2rem;
  width: 5rem;
  background-color: black;
  border-style: none;
  /* border: 1px solid red; */
  color: white;
}

.flex-item-b > button:hover {
    background-color: gray;
    cursor: pointer;
}

</style>
