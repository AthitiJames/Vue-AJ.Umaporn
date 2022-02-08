<script setup>
const accounts = [{
    name: 'salary',
    amount: 10000
},
{
    name: 'rent',
    amount: 2500
},
{
    name: 'parking fee',
    amount: 0
},
{
    name: 'car fuel',
    amount: -600
},
{
    name: 'commission',
    amount: 5500
}]
</script>

<template>
    <h1>MY ACCOUNT</h1>
    <ul v-for="account in accounts" :key="index">
        <div id="key">
            <li v-if="account.amount != 0">
                <p
                    :style="account.amount < 0 ? 'background-color:red' : 'background-color:green'"
                >Name: {{ account.name }}</p>
            </li>
            <li v-if="account.amount != 0">
                <p>Amount: {{ account.amount }}</p>
                <br />
            </li>
        </div>
    </ul>
    <p>Net Total: {{ accounts.reduce((total, account) => total + account.amount, 0) }}</p>
</template>

<style>
</style>

