<template>
  <div class="container">
    <div class="headline-a" v-for="value in story.slice(0, 1)" v-bind:key="value.title">
      <img v-bind:src="value.imageUrl" v-bind:alt="value.imageUrl">
      <span>
        <h3>{{ value.title }}</h3>
        <p>{{ value.date }}</p>
      </span>
    </div>
    <div>
      <div class="headline-b" v-for="value in story.slice(1, 4)" v-bind:key="value.title">
        <img v-bind:src="value.imageUrl" v-bind:alt="value.imageUrl">
        <div>
          <h3>{{ value.title }}</h3>
          <p>{{ value.date }}</p>
        </div>
      </div>
    </div>
    <div class="headline-c" v-for="value in story.slice(4, 5)" v-bind:key="value.title">
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
  display: flex;
  justify-content: space-evenly;
}

.headline-a {
  display: flex;
  flex-direction: column;
}

.headline-a > span {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  height: 100%;
  width: 30rem;
}

.headline-a > img, 
.headline-c > img {
  height: 9.5rem;
  width: 30rem;
  align-self: center;
}

.headline-b {
  display: grid;
  grid-template-columns: 7rem 15rem;
  margin-bottom: 5px;
}

.headline-b > div {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.headline-c > span {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  height: 166px;
}

.headline-b > img {
  height: 100px;
  width: 100px;
}
</style>

