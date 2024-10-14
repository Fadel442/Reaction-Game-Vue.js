<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Block from './components/komponen/Block.vue'
import Result from './components/komponen/Result.vue';
</script>

<template>
  <h1>Reaction Timer Game</h1>
  <button @click="start" :disabled="isPlay">Click to Play!</button>
  <Block v-if="isPlay" :delay="delay" @end="endGame"/>
  <Result v-if="showResult" :score="score" />
  <!-- <p>Reaction Time: {{ score }} ms</p> -->
</template>

<script>
  export default {
    components: { Block, Result },
    data() {
      return {
        showResult: false,
        isPlay: false,
        delay: null,
        score: null,
      }
    },
    methods: {
      start() {
        this.delay = 2000 + Math.random() * 5000
        this.isPlay = true
        this.showResult= false
      },
      endGame(reactionTime) {
        this.score = reactionTime
        this.isPlay= false
        this.showResult= true
      }
    },
  }
</script>

<style>

</style>
