<template>
  <div class="container">
    <h1>404</h1>
    <p>🍌 Oh, No, the page you are looking for isn’t available. Try to use the Back Home button below.</p>
    <p>
      <img class="bg" src="./../assets/images/404.svg" alt="404" />
      <router-link class="back-home" to="/">← Back home.</router-link>
    </p>
  </div>
</template>

<style scoped>
.bg {
  width: 100%;
  margin-bottom: 40px;
}

p {
  line-height: 40px;
  font-size: 16px;
  font-weight: bold;
}

.back-home {
  font-size: 20px;
}

.back-home:hover {
  border: none;
  font-weight: bold;
  color: #4361ee;
}
</style>
