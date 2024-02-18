<script setup lang="ts">
import {onMounted, ref, watch} from "vue";
import axios from "axios";
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
// Функция для отправки OSC сообщений теперь принимает адрес OSC в качестве параметра
const sendOscMessage = (address, id) => {
  axios.post('http://10.30.39.49:3000/send-osc', {
    address, // Используйте переданный адрес
    args: [id],
  })
      .then(() => console.log(`OSC message sent for address: ${address} with id: ${id}`))
      .catch(error => console.error('Error sending OSC message:', error));
};
watch(() => selected.value, (newVal, oldVal) => {
  if (newVal === 0 && oldVal !== 0) {
    // Здесь отправляем OSC сообщение при отжатии кнопки
    sendOscMessage('/composition/columns/1/connect', oldVal); // Используйте соответствующий адрес и предыдущее значение id как аргумент
    console.log(`Кнопка ${oldVal} отжата`);
  } else if (newVal !== 0) {
    // Остальная логика для нажатия кнопок
    console.log(`Нажата кнопка ${newVal}`);
    switch (newVal) {
      case 1:
        console.log("Нажата кнопка 1")
        sendOscMessage('/composition/columns/2/connect', 1);
        break;
      case 2:
        console.log("Нажата кнопка 2")
        sendOscMessage('/composition/columns/3/connect', 1);
        break;
      case 3:
        console.log("Нажата кнопка 3")
        sendOscMessage('/composition/columns/4/connect', 1);
        break;
      case 4:
        console.log("Нажата кнопка 4")
        sendOscMessage('/composition/columns/5/connect', 1);
        break;
      case 5:
        console.log("Нажата кнопка 5")
        sendOscMessage('/composition/columns/6/connect', 1);
        break;
      case 6:
        console.log("Нажата кнопка 6")
        sendOscMessage('/composition/columns/7/connect', 1);
        break;
      case 7:
        console.log("Нажата кнопка 7")
        sendOscMessage('/composition/columns/8/connect', 1);
        break;
      case 8:
        console.log("Нажата кнопка 8")
        sendOscMessage('/composition/columns/9/connect', 1);
        break;
      case 9:
        console.log("Нажата кнопка 9")
        sendOscMessage('/composition/columns/10/connect', 1);
        break;
      case 10:
        console.log("Нажата кнопка 10")
        sendOscMessage('/composition/columns/11/connect', 1);
        break;
      case 11:
        console.log("Нажата кнопка 11")
        sendOscMessage('/composition/columns/12/connect', 1);
        break;
      case 12:
        console.log("Нажата кнопка 12")
        sendOscMessage('/composition/columns/13/connect', 1);
        break;
      case 13:
        console.log("Нажата кнопка 13")
        sendOscMessage('/composition/columns/14/connect', 1);
        break;
      case 14:
        console.log("Нажата кнопка 14")
        sendOscMessage('/composition/columns/15/connect', 1);
        break;
      case 15:
        console.log("Нажата кнопка 15")
        sendOscMessage('/composition/columns/16/connect', 1);
        break;
      case 16:
        console.log("Нажата кнопка 16")
        sendOscMessage('/composition/columns/17/connect', 1);
        break;
    }
  }
});

const onClickContainer = () => {
  selected.value = 0
  sendOscMessage('/composition/columns/1/connect', 1);
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
      <div class="block" :class="selected == 1 ? 'selected' : ''" @click.stop="onClickBlock(1)">
        <SmallBg class="bg2"/>
        <Small class="bg1"/>
        <div class="desc">
          <div class="icon">
            <Icon1/>
          </div>
          <div class="text">
            <span>ФИДЖИТАЛ</span>
            <span style="font-size: 20px;">ЕДИНОБОРСТВО</span>
          </div>
        </div>
      </div>
      <div class="block" :class="selected == 2 ? 'selected' : ''" @click.stop="onClickBlock(2)">
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
      <div class="block" :class="selected == 3 ? 'selected' : ''" @click.stop="onClickBlock(3)">
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
      <div class="block" :class="selected == 4 ? 'selected' : ''" @click.stop="onClickBlock(4)">
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
      <div class="block" :class="selected == 5 ? 'selected' : ''" @click.stop="onClickBlock(5)">
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
      <div class="block" :class="selected == 6 ? 'selected' : ''" @click.stop="onClickBlock(6)">
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
      <div class="block" :class="selected == 7 ? 'selected' : ''" @click.stop="onClickBlock(7)">
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
      <div class="block" :class="selected == 8 ? 'selected' : ''" @click.stop="onClickBlock(8)">
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
      <div class="block" :class="selected == 9 ? 'selected' : ''" @click.stop="onClickBlock(9)">
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
      <div class="block" :class="selected == 10 ? 'selected' : ''" @click.stop="onClickBlock(10)">
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
      <div class="block" :class="selected == 11 ? 'selected' : ''" @click.stop="onClickBlock(11)">
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
      <div class="block" :class="selected == 12 ? 'selected' : ''" @click.stop="onClickBlock(12)">
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
      <div class="block" :class="selected == 13 ? 'selected' : ''" @click.stop="onClickBlock(13)">
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
      <div class="block" :class="selected == 14 ? 'selected' : ''" @click.stop="onClickBlock(14)">
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
      <div class="block" :class="selected == 15 ? 'selected' : ''" @click.stop="onClickBlock(15)">
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
      <div class="block" :class="selected == 16 ? 'selected' : ''" @click.stop="onClickBlock(16)">
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
