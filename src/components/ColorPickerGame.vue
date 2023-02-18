<template>
  <h1>Color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="color in colors" :key="color" @click="matchColor(color)">
    {{ color }}
  </button>
</template>

<script>
import { useColorPickerGame } from "../composables/color-picker";
export default {
  setup() {
    const colorsArr = ["green", "red", "blue", "purple"];

    const { colors, message, matchColor } = useColorPickerGame(colorsArr);
    return { colors, message, matchColor };
  },
};
</script>

<style></style>
