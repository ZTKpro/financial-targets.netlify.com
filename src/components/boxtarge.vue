<template>
  <div>
    <div class="box">
      <h2>months3</h2>
      <div v-for="(item,item2,item3) in months3" class="box_item" :key="item.id">
        <h3 v-for="value in item" :key="item.value">{{value}}</h3>
        <div class="box_progresbar">
          <div  class="bar"></div>
        </div>
      </div>
      <h2>months12</h2>
      <div v-for="(item,item2,item3) in months12" class="box_item" :key="item.id" >
        <h3 v-for="value in item" :key="value.id">{{value}}</h3>
        <div class="box_progresbar">
          <div class="bar"></div>
        </div>
      </div>
      <h2>years3</h2>
      <div v-for="(item,item2,item3) in years3" class="box_item" :key="item.id">
        <h3 v-for="value in item" :key="value.id">{{value}}</h3>
        <div class="box_progresbar">
          <div class="bar"></div>
        </div>
      </div>
      <h2>years6</h2>
      <div v-for="(item,item2,item3) in years6" class="box_item" :key="item.id">
        <h3 v-for="value in item" :key="value.id">{{value}}</h3>
        <div class="box_progresbar">
          <div  class="bar"></div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      months3: {
        item: {
          nameTag: "KPP",
          mycost: "100",
          cost: "690"
        },
        item2: {
          nameTag: "ASG KIT",
          mycost: "0",
          cost1: "1 286"
        },
        item3: {
          nameTag: "OWD",
          mycost: "0",
          cost2: "1 290"
        }
      },
      months12: {
        item: {
          nameTag: "DRIVING LICENSE",
          mycost: "0",
          cost: "1 999"
        },
        item1: {
          nameTag1: "MOTOBIKE",
          mycost: "0",
          cost1: "11 550"
        }
      },
      years3: {
        item: {
          nameTag: "AUDI A5",
          mycost: "0",
          cost: "66 000"
        }
      },
      years6: {
        item: {
          nameTag: "HOUSE",
          mycost: "0",
          cost: "300 000"
        }
      }
    };
  },
  methods: {
    progressBar() {

    }
  },
  created: function() {
    this.progressBar();
  }
};
</script>
<style>
h2 {
  margin: 10px;
}
.box {
  padding: 0 150px;
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
  list-style: none;
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
  width: 0.45%;
  background-color: #16cae6;
}
@media (max-width: 1200px) {
  .box {
    padding: 0 50px;
  }
}
</style>