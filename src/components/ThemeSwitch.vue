<script setup>
import { ref } from 'vue';

const isDarkMode = ref(false);

function handleButtonClick() {
  isDarkMode.value = !isDarkMode.value;
  document.body.classList.toggle('dark');
}

</script>

<template>
    <button aria-label="Light dark Mode" @click="handleButtonClick">
    <span class="material-symbols-outlined" v-if="!isDarkMode">light_mode</span>
    <span class="material-symbols-outlined" v-if="isDarkMode">dark_mode</span>
  </button>
</template>

<style lang="scss">
button {
    margin: 20px;
    background-color: darkslategray;
    color: whitesmoke;

    &:hover {
        box-shadow: 2px 2px 15px black;
    }
}

.dark {
  background-color: #303234;

  div {
    color: whitesmoke;
  }

  a {

  color:yellow;
  text-decoration: inherit;
  }

  a:hover {
    color: yellow;
  }

  button {
    background-color: whitesmoke;
    color: darkslategray;

    &:hover {
        box-shadow: 2px 2px 15px white;
    }
  }
}
</style>
