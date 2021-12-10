npm<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  components: {
  },

  data() {
    return {
      messages: [
           {
                'number' : 1,
                'image' : 'src/img/1.jpg',
                'content' : false
            },
            {
                'number' : 2,
                'image' : 'src/img/2.jpg',
                'content' : false
            },
            {
                'number' : 3,
                'image' : 'src/img/3.jpg',
                'content' : false
            },
            {
                'number' : 4,
                'image' : 'src/img/4.jpg',
                'content' : false
            },
            {
                'number' : 5,
                'image' : 'src/img/5.jpg',
                'content' : false
            },
            {
                'number' : 6,
                'image' : 'src/img/6.jpg',
                'content' : false
            },
            {
                'number' : 7,
                'image' : 'src/img/7.jpg',
                'content' : false
            },
            {
                'number' : 8,
                'image' : 'src/img/8.jpg',
                'content' : false
            },
            {
                'number' : 9,
                'image' : 'src/img/9.jpg',
                'content' : false
            },
            {
                'number' : 10,
                'image' : 'src/img/10.jpg',
                'content' : false
            },
            {
                'number' : 11,
                'image' : 'src/img/11.jpg',
                'content' : false
            },
            {
                'number' : 12,
                'image' : 'src/img/12.jpg',
                'content' : false
            },
            {
                'number' : 13,
                'image' : 'src/img/13.jpg',
                'content' : false
            },
            {
                'number' : 14,
                'image' : 'src/img/14.jpg',
                'content' : false
            },
            {
                'number' : 15,
                'image' : 'src/img/15.jpg',
                'content' : false
            },
            {
                'number' : 16,
                'image' : 'src/img/16.jpg',
                'content' : false
            },
            {
                'number' : 17,
                'image' : 'src/img/17.jpg',
                'content' : false
            },
            {
                'number' : 18,
                'image' : 'src/img/18.jpg',
                'content' : false
            },
            {
                'number' : 19,
                'image' : 'src/img/19.jpg',
                'content' : false
            },
            {
                'number' : 20,
                'image' : 'src/img/20.jpg',
                'content' : false
            },
            {
                'number' : 21,
                'image' : 'src/img/21.jpg',
                'content' : false
            },
            {
                'number' : 22,
                'image' : 'src/img/22.jpg',
                'content' : false
            },
            {
                'number' : 23,
                'image' : 'src/img/23.jpg',
                'content' : false
            },
            {
                'number' : 24,
                'image' : 'src/img/24.jpg',
                'content' : false
            },
        ],
    };
  },

  methods: {
    showPic(item){
        item.content = !item.content;
        console.log("tu as cliqué sur "+item.number);
    }
  },
});

</script>

<template>
  <h1>Weihnachtskalender 2021</h1>
  <div class="calendar">
        <div class="card" v-for="item in messages" :key="item">
            <section v-show="!item.content">
                <h1 @click="showPic(item)">{{item.number}}</h1>
            </section>
            <section v-show="item.content">
                <img :src="item.image" width="140" @click="showPic(item)">
            </section>
        </div>
    </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Mountains+of+Christmas:wght@700&display=swap');

#app {
  font-family: 'Mountains of Christmas', cursive;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 10px;
}

/* This creates a 6x4 grid with 140px wide squares */
.calendar {
  display: grid;
  grid-template-columns: repeat(6, 140px);
  grid-template-rows: repeat(4, 140px);
  gap: 20px;
  
}

.card {
    border-style: solid;
    text-align: center;
    margin-top: auto;
    margin-bottom: auto;
}
</style>
