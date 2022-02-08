<script setup>
import { ref, computed, reactive } from 'vue'
let noteInput = ref()
let notes = reactive([])
function addNote() {
    notes.push(noteInput.value)
}
// let fillterNode = computed((query) => {
//     return notes.filter(function (el) {
//         return el.toLowerCase().indexOf(query.toLowerCase()) !== -1
//     })
// })


</script>

<template>
    <div class="mb-3 xl:w-96">
        <input
            type="search"
            class="form-control block w-full px-3 py-1.5 text-base font-normal text-gray-700 bg-white bg-clip-padding border border-solid border-gray-300 rounded transition ease-in-out m-0 focus:text-gray-700 focus:bg-white focus:border-blue-600 focus:outline-none"
            id="exampleSearch"
            placeholder="Search..."
        />
    </div>

    <!-- <p v-show="notes != 0">
        Filter Note:
    <input type="text" v-model="fillterNode" />-->
    <!-- </p> -->
    New Note:
    <input type="text" v-model="noteInput" />
    <button @click="addNote">Add Note</button>
    <ul>
        <li v-for="note in notes" id="exampleSearch">{{ note }}</li>
    </ul>
</template>

<style>
</style>