<template>
  <div class="container">
    <div class="grid-item-a" v-for="value in story.slice(0, 1)" v-bind:key="value.title">
      <img v-bind:src="value.imageUrl" v-bind:alt="value.imageUrl">
      <span>
        <h3>{{ value.title }}</h3>
        <p>{{ value.date }}</p>
      </span>
    </div>

    <div>
      <div class="grid-item-b" v-for="value in story.slice(1, 4)" v-bind:key="value.title">
        <img v-bind:src="value.imageUrl" v-bind:alt="value.imageUrl">
        <div>
          <h3>{{ value.title }}</h3>
          <p>{{ value.date }}</p>
        </div>
      </div>
    </div>

    <div class="grid-item-c" v-for="value in story.slice(4, 5)" v-bind:key="value.title">
      <img v-bind:src="value.imageUrl" v-bind:alt="value.imageUrl">
      <span>
        <h3>{{ value.title }}</h3>
        <p>{{ value.date }}</p>
      </span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Headline',
  props: {
    story: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>

.container {
  /* background-color: red; */
  display: flex;
  height: 300px;
  
  /* flex-direction: column; */
  /* grid-template-columns: 1fr 1fr 1fr; */
  /* grid-template-areas:  */
    /* "container-a container-b container-c"; */
}

.grid-item-a {
  /* background-color: yellow; */
  display: flex;
  flex-direction: column;
  /* justify-content: flex-; */
  /* align-self: center; */
  /* text-align: center; */
  margin-left: 5rem;
}

.grid-item-a > span {
  /* background-color: red; */
  display: flex;
  flex-direction: column;
  margin-left: 88px;
  justify-content: space-around;
  height: 100%;
}

.grid-item-a > img,
.grid-item-c > img {
  height: 9.5rem;
  width: 30rem;
    /* margin-left: 88px; */
  align-self: center;
  /* justify-items: center; */

}

.grid-item-b {
  display: grid;
  grid-template-columns: 7rem 15rem;
  margin-bottom: 5px;
}

.grid-item-b > div {
  /* background-color: red; */
}

.grid-item-c {
  /* background-color: red ; */
    margin-left: 58px;
}

.grid-item-c > span {
  /* background-color: red !important; */
  display: flex;
  flex-direction: column;
  /* margin-left: 88px; */
  /* justify-content: space-around; */
  height: 140px;
}

.grid-item-b > img {
  height: 100px;
  width: 100px;
}


</style>

