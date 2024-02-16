<script setup lang="ts">
import {onMounted, ref, watch} from "vue";
import Big from "./components/big.vue";
import Small from "./components/small.vue";
import Icon1 from "./components/icon1.vue";
import Icon2 from "./components/icon2.vue";
import Icon3 from "./components/icon3.vue";
import Icon4 from "./components/icon4.vue";
import Icon5 from "./components/icon5.vue";
import Icon6 from "./components/icon6.vue";
import Icon7 from "./components/icon7.vue";
import Icon8 from "./components/icon8.vue";
import Icon9 from "./components/icon9.vue";
import Icon10 from "./components/icon10.vue";
import Icon11 from "./components/icon11.vue";
import Icon12 from "./components/icon12.vue";
import Icon13 from "./components/icon13.vue";
import Icon14 from "./components/icon14.vue";
import Icon15 from "./components/icon15.vue";
import Icon16 from "./components/icon16.vue";
import SmallBg from "./components/small-bg.vue";

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
    case 6: {
      console.log("Нажата кнопка 6")
      break;
    }
    case 7: {
      console.log("Нажата кнопка 7")
      break;
    }
    case 8: {
      console.log("Нажата кнопка 8")
      break;
    }
    case 9: {
      console.log("Нажата кнопка 9")
      break;
    }
    case 10: {
      console.log("Нажата кнопка 10")
      break;
    }
    case 11: {
      console.log("Нажата кнопка 11")
      break;
    }
    case 12: {
      console.log("Нажата кнопка 12")
      break;
    }
    case 13: {
      console.log("Нажата кнопка 13")
      break;
    }
    case 14: {
      console.log("Нажата кнопка 14")
      break;
    }
    case 15: {
      console.log("Нажата кнопка 15")
      break;
    }
    case 16: {
      console.log("Нажата кнопка 16")
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

onMounted(()=>{
  document.addEventListener('contextmenu', event => event.preventDefault());
})
</script>

<template>
  <div class="container" @click="onClickContainer">
    <div class="blocks">
      <div class="header">
        <Big class="bg1"/>
        <div class="desc">
          <div class="text">
            <span>PHYGITAL LAB</span>
          </div>
        </div>
      </div>
      <div class="block" :class="selected == 1 ? 'selected' : ''" @click.stop="onClickBlock(2)">
        <SmallBg class="bg2"/>
        <Small class="bg1"/>
        <div class="desc">
          <div class="icon">
            <Icon1/>
          </div>
          <div class="text">
            <span>ФИДЖИТАЛ</span>
            <span>БАСКЕТБОЛ</span>
          </div>
        </div>
      </div>
      <div class="block" :class="selected == 2 ? 'selected' : ''" @click.stop="onClickBlock(3)">
        <SmallBg class="bg2"/>
        <Small class="bg1"/>
        <div class="desc">
          <div class="icon">
            <Icon2/>
          </div>
          <div class="text">
            <span>ФИДЖИТАЛ</span>
            <span style="font-size: 20px;">СКЕЙТБОРДИНГ</span>
          </div>
        </div>
      </div>
      <div class="block" :class="selected == 3 ? 'selected' : ''" @click.stop="onClickBlock(4)">
        <SmallBg class="bg2"/>
        <Small class="bg1"/>
        <div class="desc">
          <div class="icon">
            <Icon3/>
          </div>
          <div class="text">
            <span>ФИДЖИТАЛ</span>
            <span>ХОККЕЙ</span>
          </div>
        </div>
      </div>
      <div class="block" :class="selected == 4 ? 'selected' : ''" @click.stop="onClickBlock(5)">
        <SmallBg class="bg2"/>
        <Small class="bg1"/>
        <div class="desc">
          <div class="icon">
            <Icon4/>
          </div>
          <div class="text">
            <span>СПОРТИВНОЕ</span>
            <span style="font-size: 16px;">ПРОГРАММИРОВАНИЕ</span>
          </div>
        </div>
      </div>
      <div class="block" :class="selected == 5 ? 'selected' : ''" @click.stop="onClickBlock(6)">
        <SmallBg class="bg2"/>
        <Small class="bg1"/>
        <div class="desc">
          <div class="icon">
            <Icon5/>
          </div>
          <div class="text">
            <span>ФИДЖИТАЛ</span>
            <span>БАСКЕТБОЛ</span>
          </div>
        </div>
      </div>
      <div class="block" :class="selected == 6 ? 'selected' : ''" @click.stop="onClickBlock(7)">
        <SmallBg class="bg2"/>
        <Small class="bg1"/>
        <div class="desc">
          <div class="icon">
            <Icon6/>
          </div>
          <div class="text">
            <span>STANDOFF 2 +</span>
            <span>ЛАЗЕРТАГ</span>
          </div>
        </div>
      </div>
      <div class="block" :class="selected == 7 ? 'selected' : ''" @click.stop="onClickBlock(8)">
        <SmallBg class="bg2"/>
        <Small class="bg1"/>
        <div class="desc">
          <div class="icon">
            <Icon7/>
          </div>
          <div class="text">
            <span>ФИДЖИТАЛ</span>
            <span>ГОНКИ</span>
          </div>
        </div>
      </div>
      <div class="block" :class="selected == 8 ? 'selected' : ''" @click.stop="onClickBlock(9)">
        <SmallBg class="bg2"/>
        <Small class="bg1"/>
        <div class="desc">
          <div class="icon">
            <Icon8/>
          </div>
          <div class="text">
            <span>ГОНКИ</span>
            <span>ДРОНОВ</span>
          </div>
        </div>
      </div>
      <div class="block" :class="selected == 9 ? 'selected' : ''" @click.stop="onClickBlock(10)">
        <SmallBg class="bg2"/>
        <Small class="bg1"/>
        <div class="desc">
          <div class="icon">
            <Icon9/>
          </div>
          <div class="text">
            <span>ФИДЖИТАЛ</span>
            <span>ФУТБОЛ</span>
          </div>
        </div>
      </div>
      <div class="block" :class="selected == 10 ? 'selected' : ''" @click.stop="onClickBlock(11)">
        <SmallBg class="bg2"/>
        <Small class="bg1"/>
        <div class="desc">
          <div class="icon">
            <Icon10/>
          </div>
          <div class="text">
            <span>SPEEDRUN +</span>
            <span>СУПЕРФИНАЛ</span>
          </div>
        </div>
      </div>
      <div class="block" :class="selected == 11 ? 'selected' : ''" @click.stop="onClickBlock(12)">
        <SmallBg class="bg2"/>
        <Small class="bg1"/>
        <div class="desc">
          <div class="icon">
            <Icon11/>
          </div>
          <div class="text">
            <span>БИТВА</span>
            <span>РОБОТОВ</span>
          </div>
        </div>
      </div>
      <div class="block" :class="selected == 12 ? 'selected' : ''" @click.stop="onClickBlock(13)">
        <SmallBg class="bg2"/>
        <Small class="bg1"/>
        <div class="desc">
          <div class="icon">
            <Icon12/>
          </div>
          <div class="text">
            <span>ФИДЖИТАЛ</span>
            <span>MOBA. DOTA 2</span>
          </div>
        </div>
      </div>
      <div class="block" :class="selected == 13 ? 'selected' : ''" @click.stop="onClickBlock(14)">
        <SmallBg class="bg2"/>
        <Small class="bg1"/>
        <div class="desc">
          <div class="icon">
            <Icon13/>
          </div>
          <div class="text">
            <span>CS2 +</span>
            <span>ЛАЗЕРТАГ</span>
          </div>
        </div>
      </div>
      <div class="block" :class="selected == 14 ? 'selected' : ''" @click.stop="onClickBlock(15)">
        <SmallBg class="bg2"/>
        <Small class="bg1"/>
        <div class="desc">
          <div class="icon">
            <Icon14/>
          </div>
          <div class="text">
            <span>МИР ТАНКОВ +</span>
            <span>СУПЕРФИНАЛ</span>
          </div>
        </div>
      </div>
      <div class="block" :class="selected == 15 ? 'selected' : ''" @click.stop="onClickBlock(16)">
        <SmallBg class="bg2"/>
        <Small class="bg1"/>
        <div class="desc">
          <div class="icon">
            <Icon15/>
          </div>
          <div class="text">
            <span>WARFACE +</span>
            <span>ЛАЗЕРТАГ</span>
          </div>
        </div>
      </div>
      <div class="block" :class="selected == 16 ? 'selected' : ''" @click.stop="onClickBlock(17)">
        <SmallBg class="bg2"/>
        <Small class="bg1"/>
        <div class="desc">
          <div class="icon">
            <Icon16/>
          </div>
          <div class="text">
            <span>ФИДЖИТАЛ</span>
            <span>MOBA. MLBB</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>
