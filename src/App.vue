<script setup lang="ts">
import { ref } from 'vue'
import Box from '@/components/Box.vue'
import Tile from '@/components/Tile.vue'
import DetailsForm from '@/components/DetailsForm.vue'

const boxes = ref([
  {
    title: '<h3>Curious about the <div class="text-primary d-inline">StockX</div> Mystery Box?</h3>',
    texts: ['Experience the thrill of unboxing cutting-edge gadgets with Stockx Mystery Boxes. Each box is a treasure trove of high-quality electronics, handpicked to elevate your tech game.', 'Expect the unexpected! Our boxes are packed with the latest gadgets, from smartphones to gaming consoles, ensuring you get the best tech surprises every time.'
    ], img: {
      fileName: 'box1.png',
      alt: 'Box 1'
    }
  },
  {
    title: '<h3>Why is everyone buzzing about these boxes?</h3>',
    texts: ['StockX Mystery Boxes are not just about products; they’re about the experience. Imagine the excitement of unveiling top-tier electronics at a fraction of the cost.', 'Our boxes include a variety of premium tech items, making it a must-have for every tech enthusiast. Join the buzz and see why everyone is raving about the unbeatable value and surprise factor of Stockx Mystery Boxes!'],
    img: { fileName: 'box2.png', alt: 'Box 2' }
  }
])
const tiles = ref([{
  title: 'How can I win?',
  text: 'Thanks to your membership, you  also participate in our contest to win the iPhone15. We sellect a winner among every 600 participants. The next winner will be selected on 06.10.2023, and will be notified directly by e-mail. If the reward is out of stock, the winner will receive a similar product of equal or greater value instead.'
},
  {
    title: 'No hidden fees?',
    text: 'We ensure that our members are provided with a detailed history of transactions so that they know exactly what they are paying for. Credit card information is only required to facilitate future purchases. There will be no charges on your credit card statement if you do not upgrade to PREMIUM membership and do not make a purchase.'
  }, {
    title: 'Why do we need your billing information?',
    text: 'By joining this service, you will receive a 5-day trial of our partner\'s program. If you continue with a subscription beyond the 5-day trial period, you will be charged an amount on your credit card which varies depending on the choice of the tariff. When your contribution is deducted from your credit card or other payment method, you will have access to these services which are reserved exclusively for members of our partner\'s website.'
  }])
</script>

<template>
  <div class="d-flex flex-row">
    <img class="w-50" alt="Group of products" src="./assets/group.png" />
    <div class="d-flex flex-column">
      <h1 class="mb-0">Chance to win a StockX Mystery Box today!</h1>
      <p class="text-lg mt-0 ">Unleash the Excitement of Mystery Electronics</p>
      <details-form />
    </div>
  </div>
  <div class="d-flex justify-center flex-column">
    <h2 class="mb-0 text-align-center">Top Tech Mystery Box
      at Unbeatable Prices</h2>
    <p class="text-primary text-lg text-align-center font-weight-500 my-05">Fast shipping | Easy returns | Special
      discounts
      for
      students</p>
  </div>
  <div>
    <box v-for="(box, index) in boxes" :key="box.title" :texts="box.texts" :img="box.img"
         :is-reversed="index % 2 !== 0">
      <div v-html="box.title"></div>
    </box>
  </div>
  <div class="d-flex flex-row bg-secondary">
    <tile class="mx-1" v-for="tile in tiles" :key="tile.title" :title="tile.title" :text="tile.text" />
  </div>
  <footer>
    <p class="text-align-center">We accept the following credit cards</p>
    <img alt="Accepted credit cards" class="w-100" src="./assets/cards%201.png" />
  </footer>
</template>

<style scoped>

</style>
