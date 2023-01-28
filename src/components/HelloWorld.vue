<template>
  <div class="container">
  <img class="top-image" alt="Vue logo" src="../assets/portfolio.jpg">
    <div class="introduction mb-50">
      <h2>自己紹介</h2>
      <p>こんにちは。すみすです。大学1年生です。</p>
    </div>
    <h2>SKILL</h2>
    <div class="graphs">
      <template v-for="graph in graphs" :key="graph">
        <Graph :skillname="graph.skill" :numbername="graph.number" class="graph"/>
      </template>
    </div>
    <h2>WORKS</h2>
    <div class="works">
      <template v-for="content in contents" :key="content">
        <Work :imgname="content.img" :urlname="content.url" :titlename="content.title" :username="content.text" class="work"/>
      </template>
    </div>
  </div>
</template>

<script>
import Work from './Work.vue'
import Graph from './Graph.vue'

export default {
  name: 'HelloWorld',
  components: {
    Work,
    Graph
  },
  data(){
    return{
      contents:[
        {
          title:"WORK1",
          text:"これはwork1です。",
          url:"https://sota0110.github.io/typingGame-vue/",
          img:require("../assets/typing.png")
        },{
          title:"WORK2",
          text:"これはwork2です。",
          url:"https://sota0110.github.io/typingGame-vue/",
          img:require("../assets/typing.png")
        },{
          title:"WORK3",
          text:"これはwork3です。",
          url:"https://sota0110.github.io/typingGame-vue/",
          img:require("../assets/typing.png")
        },{
          title:"WORK4",
          text:"これはwork4です。",
          url:"https://sota0110.github.io/typingGame-vue/",
          img:require("../assets/typing.png")
        }
      ],
      graphs:[
        {
          skill:"Javascript",
          number:4
        },{
          skill:"Python",
          number:2
        },{
          skill:"R",
          number:1
        },{
          skill:"HTML/CSS",
          number:3
        },{
          skill:"C",
          number:5
        }
      ]
    }
  }
}
</script>

<style>
  .mb-50{
    margin-bottom: 50px;
  }

  .top-image{
    width: 101.3%;
    margin-top: -60px;
    margin-left: -8px;
  }

  .work{
    margin: 20px 20px;
    display: inline-block;
    width: 30%;
    text-align: center;
    color: black;
    text-decoration: none
  }

  .work img{
    width: 100%;
  }

  .work h3{
    font-size: 20px;
  }

  .work img{
    border: 3px solid gray;
    border-radius: 4px;
  }
</style>