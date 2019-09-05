<template>
  <div class="box">
    <h2>3 MONTHS</h2>

    <div   id="box" class="box_item">
      <h3>{{ months3.name }}</h3>
      <p class="item_cost">{{months3.cost}}</p>
      <div class="box_progresbar">
        <div style="width:32%" class="bar"></div>
      </div>
    </div>

    <div id="box" class="box_item">
      <h3>{{ months3.name1 }}</h3>
      <p class="item_cost">{{months3.cost1}}</p>
      <div class="box_progresbar">
        <div style="width:32%" class="bar"></div>
      </div>
    </div>

    <div id="box" class="box_item">
      <h3>{{ months3.name2 }}</h3>
      <p class="item_cost">{{months3.cost2}}</p>
      <div class="box_progresbar">
        <div style="width:32%" class="bar"></div>
      </div>
    </div>

    <h2>12 MONTHS</h2>

    <div id="box" class="box_item">
      <h3>{{ months12.name }}</h3>
      <p class="item_cost">{{months12.cost}}</p>
      <div class="box_progresbar">
        <div style="width:62%" class="bar"></div>
      </div>
    </div>

    <div id="box" class="box_item">
      <h3>{{ months12.name1 }}</h3>
      <p class="item_cost">{{months12.cost1}}</p>
      <div class="box_progresbar">
        <div style="width:62%" class="bar"></div>
      </div>
    </div>

    <h2>3 YEARS</h2>

    <div id="box" class="box_item">
      <h3>{{ years3.name }}</h3>
      <p class="item_cost">{{years3.cost}}</p>
      <div class="box_progresbar">
        <div style="width:2%" class="bar"></div>
      </div>
    </div>

    <h2>6 YEARS</h2>

    <div id="box" class="box_item">
      <h3>{{ years6.name }}</h3>
      <p class="item_cost">{{years6.cost}}</p>
      <div class="box_progresbar">
        <div style="width:2%" class="bar"></div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      months3: {
        name: "KPP",
        cost: "690,00 zł",
        mycost: "690,00 zł",

        name1: "ASG KIT",
        cost1: "1 286,00 zł",
        mycost: "690,00 zł",

        name2: "OWD",
        cost2: "1 290,00 zł",
        mycost: "690,00 zł"
      },
      months12: {

        name: "DRIVING LICENSE",
        cost: "1 990,00 zł",
        mycost: "690,00 zł",

        name1: "MOTOBIKE",
        cost1: "11 550,00 zł",
        mycost: "690,00 zł"
      },
      years3: {
        name: "AUDI A5",
        cost: "66 000,00 zł",
        mycost: "690,00 zł"
      },
      years6: {
        name: "HOUSE",
        cost: "300 000,00 zł",
        mycost: "690,00 zł"
      }
    };
  },
  methods: {
    progressBar() {
      for (let i = 0; i < 10; i++) {
        console.log('aa');
      }
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
  background-color: #16cae6;
}
</style>