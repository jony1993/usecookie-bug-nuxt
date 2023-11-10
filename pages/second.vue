<template>
<div>
    <h1>Cookie second site:</h1>
    <p>We call useCookie('test') to fetch the value: {{ cookie }}</p>
    <ul>
        <li>Check cookies in Chrome Dev Tools</li>
        <li>Navigate back using browser back and check cookie again</li>
        <li>Navigate back using NuxtLink: <NuxtLink to="/">Navigate to first page via NuxtLink</NuxtLink></li>
    </ul>
</div>
</template>
<script setup>
const cookie = useCookie('test').value;
</script>