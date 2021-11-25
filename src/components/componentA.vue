<template>
  <button @click="changeView(1)">1</button>
  <button @click="changeView(2)">2</button>
  <button @click="changeView(123)">123</button>
  <div class="c1" v-if="view === 1">
    <p>hello world</p>
    {{data}}
  </div>
  <div v-else>
    <p>
      nothing
    </p>
  </div>
  <div class="c2" v-if="view === 2">
    <input type="text" v-model="text"/>
    <p>
      {{text}}
    </p>
  </div>
  <div v-else>
    <p>
      nothing
    </p>
  </div>
</template>

<script setup>
import { ref } from "@vue/reactivity"

const data = "hello young"
const text = ref("123")
const view = ref(1)
const changeView = (index) => {
  view.value = index
}
</script>

<style>

</style>