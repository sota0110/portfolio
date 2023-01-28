<template>
    <div class="container">
      <p>{{ skillname }}</p>
      <div class="skillGraph-wrapper">
        <div :style="gauge" class="skillGraph"></div>
      </div>
    </div>
</template>
  
  <script>
  export default {
    name: 'performance-graph',
    props:{
      skillname: String,
      numbername: String
    },
    computed:{
      gauge:function(){
        return{
          'width':15*this.numbername+"%"
        }
      }
    }
  }
</script>

<style scoped>
  .skillGraph-wrapper{
    border-left: 3px solid gray;
    padding: 10px 0;
  }

  .skillGraph{
    background-color: skyblue;
    padding: 15px 0;
  }
</style>