<template>
  <div id="app">
    <Navbar v-bind:navbarItem="mediumData.navbarItem"/>
    <Headline v-bind:story="mediumData.story"/>
    <Banner v-bind:banner="mediumData.banner"/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import Navbar from './components/Navbar.vue'
import Headline from './components/Headline.vue'
import Banner from './components/Banner.vue'

@Component({
  name: 'App',
  components: {
    Navbar,
    Headline,
    Banner
  }
})

class App extends Vue {
  public mediumData: object = {
    navbarItem: ['Home', 'ONEZERO', 'ELEMENTAL', 'GEN', 'STARTUPS', 'SELF', 'TECH', 'HEATED', 'ZORA', 'DESIGN', 'CULTURE', 'HUMAN PARTS', 'MORE'],
    story: [
      {
        title: 'The Masochistic Gaming Ecstasy of Super Mario ‘Kaizo’ Hacks',
        imageUrl: 'https://cdn-images-1.medium.com/max/1200/1*-56QseoRtVrX9d0W-44OgQ.png',
        subtitle: 'A nightmare from your childhood, this Mario exists to break you. But you will find meaning in the pain.',
        desc: 'Lizz Schumer was diagnosed with fibromyalgia when she was 25 years old. Although she first experienced a variety of confusing symptoms several years earlier when she was in college.',
        date: 'a few hours ago 12 min read'
      },
      {
        title: 'Managing Chronic Illness in the Workplace',
        imageUrl: 'https://cdn-images-1.medium.com/max/1600/1*0hwxuu7eQeaWf_blXx9xMQ.gif',
        subtitle: 'It’s a problem shared by millions of Americans. Experts, patients, and researchers offer ways to cope.',
        desc: 'Every night for the past several weeks, a cheerful, plump plumber arrives at my apartment and brutalizes me. Sometimes, his overalls are blue, other times red, but his cruel smile is constant. His mustache never changes. Something has gone bad with this version of Nintendo’s enduring, pipe-diving mascot Mario. He’s been modified, his game hacked into a nightmarishly difficult torture chamber that I have foolishly dedicated myself to successfully navigating.',
        date: 'Jun 28 7 min read'
      },
      {
        title: 'Sarah Sanders Doesn’t Deserve Reporters',
        imageUrl: 'https://cdn-images-1.medium.com/max/1600/1*fa8GQ21bEZr3O2D5WamsNw.jpeg',
        subtitle: 'Hobnobbing with the departing press secretary makes light of the callous acts of the administration she served',
        desc: 'It took me one hour to birth a healthy daughter — and another four years to conceive a healthy version of motherhood. A version that didn’t require the death of my dreams or my former self.',
        date: 'Jun 28 4 min read'
      },
      {
        title: 'Some Lessons Should not Be Handed Down',
        imageUrl: 'https://cdn-images-1.medium.com/max/1600/1*fa8GQ21bEZr3O2D5WamsNw.jpeg',
        subtitle: 'Despite what my auntie taught me, being a mom doesn’t require martyrdom',
        desc: 'Every night for the past several weeks, a cheerful, plump plumber arrives at my apartment and brutalizes me. Sometimes, his overalls are blue, other times red, but his cruel smile is constant. His mustache never changes. Something has gone bad with this version of Nintendo’s enduring, pipe-diving mascot Mario. He’s been modified, his game hacked into a nightmarishly difficult torture chamber that I have foolishly dedicated myself to successfully navigating.',
        date: 'Jun 28 4 min read'
      },
      {
        title: 'Managing Chronic Illness in the Workplace',
        imageUrl: 'https://cdn-images-1.medium.com/max/1600/1*0hwxuu7eQeaWf_blXx9xMQ.gif',
        subtitle: 'It’s a problem shared by millions of Americans. Experts, patients, and researchers offer ways to cope.',
        desc: 'Every night for the past several weeks, a cheerful, plump plumber arrives at my apartment and brutalizes me. Sometimes, his overalls are blue, other times red, but his cruel smile is constant. His mustache never changes. Something has gone bad with this version of Nintendo’s enduring, pipe-diving mascot Mario. He’s been modified, his game hacked into a nightmarishly difficult torture chamber that I have foolishly dedicated myself to successfully navigating.',
        date: 'Jun 28 7 min read'
      },
      {
        title: 'Sarah Sanders Doesn’t Deserve Reporters’ “Civility”',
        imageUrl: 'https://cdn-images-1.medium.com/max/1600/1*fa8GQ21bEZr3O2D5WamsNw.jpeg',
        subtitle: 'Hobnobbing with the departing press secretary makes light of the callous acts of the administration she served',
        desc: 'It took me one hour to birth a healthy daughter — and another four years to conceive a healthy version of motherhood. A version that didn’t require the death of my dreams or my former self.',
        date: 'Jun 28 4 min read'
      },
      {
        title: 'Some Lessons Should not Be Handed Down',
        imageUrl: 'https://cdn-images-1.medium.com/max/1600/1*fa8GQ21bEZr3O2D5WamsNw.jpeg',
        subtitle: 'Despite what my auntie taught me, being a mom does not require martyrdom',
        desc: 'Every night for the past several weeks, a cheerful, plump plumber arrives at my apartment and brutalizes me. Sometimes, his overalls are blue, other times red, but his cruel smile is constant. His mustache never changes. Something has gone bad with this version of Nintendo’s enduring, pipe-diving mascot Mario. He’s been modified, his game hacked into a nightmarishly difficult torture chamber that I have foolishly dedicated myself to successfully navigating.'
      }
    ],
    banner: {
      title: 'Never miss a story',
      message: 'Sign for Medium Daily Digest and get the best of Medium, tailored for you.'
    }
  }

  private created = () => {
    console.log(this)
  }

}

export default App
</script>

<style>
* {
  margin: 0px;
  padding: 0px;
}
</style>
