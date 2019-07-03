<template>
  <div class="container">
    <div class="flex-item">
      <div class="flex-item-a">
        <h3>Featured for members</h3>
        <p class="color-lightgrey">MORE ></p>
      </div>
      <div class="flex-item-a-a" v-for="(value, index) in story" v-bind:key="index">
        <div class="flex-item-a-b">
          <h3>{{ value.title }}</h3>
          <p>{{ limitWordCount(value.desc, 15)   }}</p>
          <p class="color-lightgrey">{{ limitWordCount(value.subtitle, 15) }}</p>
          <p>{{ value.date }}</p>
        </div>
        <img class="story-image" v-bind:src="value.imageUrl" v-bind:alt="value.imageUrl">
      </div>
    </div>
    <div class="flex-item-b">
      <h3 class="title">Popular on Medium</h3>
      <div class="flex-item-b-a" v-for="(value, index) in story" v-bind:key="index">
        <p>{{ index + 1 }}</p>
        <div class="">
          <h3>{{ value.title }}</h3>
          <div>
            <p class="color-lightgrey">{{ limitWordCount(value.subtitle, 5) }}</p>
            <p>{{ value.date }}</p>
          </div>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'Story',
  props: {
    story: {
      type: Array,
      required: true
    }
  },
  methods: {
    // Limit word by x number
    limitWordCount(payload, endNumber) {
      let str = payload.split(' ').slice(0, endNumber).join(' ')
      return str
    }
  }
}
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: row;
  margin: auto;
  width: 75%;
}

.flex-item {
  display: flex;
  flex-direction: column;
}

.flex-item-a {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  position: relative;
  margin-bottom: 10px;
}

.flex-item-a:before {
  position: absolute;
  background: linear-gradient(to right, brown 11rem, #ccc 50px);
  height: 2px;
  content: ''; 
  bottom: 0;
  right: 0;
  left: 0;
}

.flex-item-a > p {

}

.color-lightgrey {
  color: rgba(0,0,0,.54);
}

.flex-item-a-a {
  display: flex;
  justify-content: space-between;
  margin-bottom: 3rem;
}

.flex-item-a-b {
  width: 100%;
}

.flex-item-a-b > p {
  margin-bottom: 5px;
  margin-top: 5px;
}

.title {
  border-bottom: 2px solid #ccc;
}

.flex-item-b {
  display: flex;
  flex-direction: column;
  width: 25%;
  margin: auto;
  margin-top: 20px;
}

.flex-item-b-a {
  display: flex;
  flex-direction: row;
  margin-top: 1rem;
}

.flex-item-b-a > p {
  width: 10%;
  text-align: center;
  padding-top: 2px;
}

.flex-item-b-a > div {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  width: 90%;
  height: 100px;
}

.story-image {
  height: 8rem;
  width: 8rem;
}
</style>
