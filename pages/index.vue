<template>
    <div>
        <h1>Cookie first site:</h1>
        <ol>
            <li>Set the cookie: <button @click="setCookie()">Set the cookie</button></li>
            <li>Check cookies in Chrome Dev Tools</li>
            <li>
                Navigate to second page via NuxtLink: <NuxtLink to="/second">Navigate to second page via NuxtLink</NuxtLink>
            </li>
        </ol>
    </div>
  </template>
  
<script setup>
  function setCookie() {
    const dataExpiresAt = new Date(
      new Date().getTime() + 365 * 24 * 60 * 60 * 1000
    );
  
    useCookie('test', {
      path: '/',
      expires: dataExpiresAt,
    }).value = true;
  }
  </script>
  