<template>
    <nav class="flex">
      <img src="src/assets/logo.svg" alt="logo">
     <ul class="flex">
      <li>Features</li>
      <li>Company</li>
      <li>Careers</li>
      <li>About</li>
      <li>Login</li>
      <li>Register</li>
     </ul>
    </nav>
</template>

<style scoped>
 .flex {
     display: flex;
     gap: var(--gap, 2em);
 }

 nav {
     margin: 0;
 }
</style>