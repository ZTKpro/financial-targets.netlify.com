<template>
<div>
    <div class="box">
        <h2>months3</h2>
        <div v-for="item in months3" class="box_item" :key="item.id">
            <h3>{{item.nameTarget}}</h3>
            <p id="itemMycost" class="hidden">{{item.mycost}}</p>
            <p id="itemCost">{{item.cost}}</p>
            <div class="box_progresbar">
                <div class="bar"></div>
            </div>
        </div>
        <h2>months12</h2>
        <div v-for="item in months12" class="box_item" :key="item.id">
            <h3>{{item.nameTarget}}</h3>
            <p id="itemMycost" class="hidden">{{item.mycost}}</p>
            <p id="itemCost">{{item.cost}}</p>
            <div class="box_progresbar">
                <div class="bar"></div>
            </div>
        </div>
        <h2>years3</h2>
        <div v-for="item in years3" class="box_item" :key="item.id">
            <h3>{{item.nameTarget}}</h3>
            <p id="itemMycost" class="hidden">{{item.mycost}}</p>
            <p id="itemCost">{{item.cost}}</p>
            <div class="box_progresbar">
                <div class="bar"></div>
            </div>
        </div>
        <h2>years6</h2>
        <div v-for="item in years6" class="box_item" :key="item.id">
            <h3>{{item.nameTarget}}</h3>
            <p id="itemMycost" class="hidden">{{item.mycost}}</p>
            <p id="itemCost">{{item.cost}}</p>
            <div class="box_progresbar">
                <div class="bar"></div>
            </div>
        </div>
    </div>
</div>
</template>

<script>
import mont3 from "./jsonFiles/month3.json"
import mont12 from "./jsonFiles/month12.json"
import year3 from "./jsonFiles/years3.json"
import year6 from "./jsonFiles/years6.json"
export default {
    data() {
        return {
            months3: mont3,
            months12: mont12,
            years3: year3,
            years6: year6,
        };
    },
    methods: {
        progresBar: function () {
            const itemMycost = document.querySelectorAll("#itemMycost")
            const itemCost = document.querySelectorAll("#itemCost")
            const bar = document.querySelectorAll(".bar")
            for (let i = 0; i < itemCost.length; i++) {
                let iC = itemCost[i].textContent
                let iM = itemMycost[i].textContent
                let bi = bar[i]
                let alfa = Math.round(iM / iC * 100)
                bi.style.width = alfa + "%"
            }
        }
    },
    mounted: function () {
        this.progresBar()
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

.box_progresbar>.bar {
    height: 100%;
    background-color: #16cae6;
}

.hidden {
    opacity: 0;
}

@media (max-width: 1200px) {
    .box {
        padding: 0 50px;
    }
}
</style>
