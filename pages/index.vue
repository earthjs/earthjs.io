<template>
    <div id="app-eq">
        <div class="set-options"></div>
        <svg id="earth" class="ea-layer ea-1"></svg>
        <div class="c-canvas">
            <canvas  class="canvas ea-layer ea-2"></canvas>
            <canvas  class="canvas ea-layer ea-3"></canvas>
        </div>
        <div class="set-options2">
        </div>
        <script type='text/javascript' src="./ex/index.js"></script>
    </div>
</template>

<script>
/*eslint no-console: 0 */
export default {
    methods: {
        mag(e) {
            const value = +e.target.value;
            window.g.eQuakeApp.mag(value);
        },
        v: '3'
    },
}
// <label><input @click="mag" type="radio" name="magnitue" v-model="v" value="6"> mag:6</input></label>
// <label><input @click="mag" type="radio" name="magnitue" v-model="v" value="5"> mag:5</input></label>
// <label><input @click="mag" type="radio" name="magnitue" v-model="v" value="4"> mag:4</input></label>
// <label><input @click="mag" type="radio" name="magnitue" v-model="v" value="3"> mag:3</input></label>
// <label><input @click="mag" type="radio" name="magnitue" v-model="v" value="2"> mag:2</input></label>
</script>

<style>
#earth, .c-canvas {
    left: -200px;
}
.c-canvas {
    position: absolute;
}
input[type="range"] {
    padding-bottom: 5px;
}
.top {
    padding: 10px 0 0 15px;
}
.set-options {
    top: 40px;
}
.set-options button {
    margin-left: 15px;
}
.set-options2 {
    position: absolute;
    margin-top: 70px;
    margin-left: 5px;
    z-index: 5;
}
.set-options2 label {
    display: block;
    margin: 10px 0 0 15px;
}
</style>
