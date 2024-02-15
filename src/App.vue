<script setup lang="ts">
import {ref, watch} from "vue";

const selected = ref(0);

watch(() => selected.value, (id: typeof selected.value) => {
  switch (id) {
    case 1: {
      console.log("Нажата кнопка 1")
      break;
    }
    case 2: {
      console.log("Нажата кнопка 2")
      break;
    }
    case 3: {
      console.log("Нажата кнопка 3")
      break;
    }
    case 4: {
      console.log("Нажата кнопка 4")
      break;
    }
    case 5: {
      console.log("Нажата кнопка 5")
      break;
    }
  }
})

const onClickContainer = () => {
  selected.value = 0
}

const onClickBlock = (id: number) => {
  if (selected.value === id) {
    selected.value = 0
  } else {
    selected.value = id
  }
}
</script>

<template>
  <div class="container" @click="onClickContainer">
    <div class="blocks">
      <div class="block" :class="selected == 1 ? 'selected' : ''" @click.stop="onClickBlock(1)">

      </div>
      <div class="block" :class="selected == 2 ? 'selected' : ''" @click.stop="onClickBlock(2)">

      </div>
      <div class="block" :class="selected == 3 ? 'selected' : ''" @click.stop="onClickBlock(3)">

      </div>
      <div class="block" :class="selected == 4 ? 'selected' : ''" @click.stop="onClickBlock(4)">

      </div>
      <div class="block" :class="selected == 5 ? 'selected' : ''" @click.stop="onClickBlock(5)">

      </div>
      <div class="block" :class="selected == 6 ? 'selected' : ''" @click.stop="onClickBlock(6)">

      </div>
      <div class="block" :class="selected == 7 ? 'selected' : ''" @click.stop="onClickBlock(7)">

      </div>
      <div class="block" :class="selected == 8 ? 'selected' : ''" @click.stop="onClickBlock(8)">

      </div>
      <div class="block" :class="selected == 9 ? 'selected' : ''" @click.stop="onClickBlock(9)">

      </div>
      <div class="block" :class="selected == 10 ? 'selected' : ''" @click.stop="onClickBlock(10)">

      </div>
      <div class="block" :class="selected == 11 ? 'selected' : ''" @click.stop="onClickBlock(11)">

      </div>
      <div class="block" :class="selected == 12 ? 'selected' : ''" @click.stop="onClickBlock(12)">

      </div>
      <div class="block" :class="selected == 13 ? 'selected' : ''" @click.stop="onClickBlock(13)">

      </div>
      <div class="block" :class="selected == 14 ? 'selected' : ''" @click.stop="onClickBlock(14)">

      </div>
      <div class="block" :class="selected == 15 ? 'selected' : ''" @click.stop="onClickBlock(15)">

      </div>
      <div class="block" :class="selected == 16 ? 'selected' : ''" @click.stop="onClickBlock(16)">

      </div>
      <div class="block" :class="selected == 17 ? 'selected' : ''" @click.stop="onClickBlock(17)">

      </div>
    </div>
  </div>
</template>

<style scoped>

</style>
