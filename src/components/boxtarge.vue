<template>
  <div  class="box">
    <div id="box" class="box_item">
      <h2>{{ dream1.name }}</h2>
      <p class="item_cost">{{dream1.cost}}</p>
      <div class="box_progresbar">
        <div class="bar"></div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      dream1: {
        name: "ASG KIT",
        cost: "1 286,00 zł"
      },
    };
  },
  methods: {
    appendDreams() {
        console.log('aa')
    }
  },
  created: function() {
    this.appendDreams();
  }
};
</script>
<style>
.box{
    padding:0 150px;
}
.box_item {
  height: 85px;
  background-color: white;
  border: 1px solid rgb(221, 221, 221);
  padding: 25px;
  margin: 10px auto;
  border-radius: 5px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: relative;
  overflow: hidden;
}
.box_progresbar {
  height: 5px;
  width: 100%;
  position: absolute;
  left: 0px;
  bottom: 0px;
  background-color: rgb(192, 192, 192);
}
.box_progresbar > .bar {
  height: 100%;
  width: 30%;
  background-color: #16cae6;
}
</style>