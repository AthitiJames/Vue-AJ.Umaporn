<script setup>
let number = 1
const color = 'color: green'
const imagePath = '../public/images/camylla-battani-A5E-ym6WyGM-unsplash.jpg'
const count = 1
const username = ''

const depositamt = 1000

const foods = ['steak', 'salad', 'tomyum', 'fried rice']
const students = [
    { stdId: 1234, stdName: 'Hataiwan Mekvee' },
    { stdId: 1235, stdName: 'Sarin Weerakun' },
    { stdId: 1236, stdName: 'Supichaya Muennuch' }
]

const course = {
    title: 'INT203 Client II',
    credit: 3,
    class: 'lecture & lab'
}

</script>

<template>
    <div>
        <h1 class="tracking-widest">Hello, Vue.js</h1>
        <h2>V-TEXT</h2>
        <p v-text="number"></p>
        <p>{{ number }}</p>    <!--shot-->
    </div>

    <br />
    <h2>V-BIND</h2>
    <p :style="color">V-bind shot</p>
    <p v-bind:style="color">V-bind</p>
    <img src="./assets/logo.png" />
    <img :src="imagePath" alt srcset />

    <h2>V-show</h2>
    <p v-show="count">Counter: 1</p>
    <p>UserName:{{ username }}</p>
    <p v-show="!username" style="color:red">Plasse Enter your name!</p>

    <h2>v-if/v-else/v-else-if</h2>
    <p>Deposit Amount: {{ depositamt }}</p>
    <p v-if="depositamt <= 100">Interest: {{ depositamt * 0.05 }}</p>
    <p v-else-if="depositamt <= 500">Interest: {{ depositamt * 0.1 }}</p>
    <p v-else>Interest: {{ depositamt * 0.15 }}</p>

    <h2>v-for</h2>
    <h1>Food List</h1>

    <ul>
        <li v-for="(food, index) in foods" :key="index">{{ food }}</li>
    </ul>

    <ul>
        <li v-for="student in students" :key="students.stdId">
            {{ student.stdId }}:
            {{ student.stdName }}
        </li>
    </ul>

    <ul>
        <li v-for="(propValue, propKey, index) in course" :key="index">
            #{{ index }} - {{ propKey }}:
            {{ propValue }}
        </li>
    </ul>
</template>

<style>
</style>
