<template>
    <div id="app-eq">
        <div class="set-options"></div>
        <svg id="earth"></svg>
        <canvas class="canvas"></canvas>
        <div class="set-options2">
            <label><input @click="mag" type="radio" name="magnitue" v-model="v" value="5"> mag:5</input></label>
            <label><input @click="mag" type="radio" name="magnitue" v-model="v" value="4"> mag:4</input></label>
            <label><input @click="mag" type="radio" name="magnitue" v-model="v" value="3"> mag:3</input></label>
            <label><input @click="mag" type="radio" name="magnitue" v-model="v" value="2"> mag:2</input></label>
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
            window.p.eQuakeApp.mag(value);
        },
        v: '3'
    },
}
</script>

<style>
#earth, .canvas {
    left: -200px;
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
