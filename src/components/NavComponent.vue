<template>
  <nav>
    <ul class="flex" role="list">
      <img src="src/assets/logo.svg" alt="logo" class="logo" />
      <li>
        <details>
          <summary>Features</summary>
          <div class="card">
            <li :key="i" v-for="(feature, i) in features">
              <v-img :src="import(`../assests/${icons[i].icon}`)" />
              {{ feature }}
            </li>
          </div>
        </details>
      </li>
      <li>
        <details>
          <summary>Company</summary>
          <div class="card">
            <li :key="i" v-for="(product, i) in company">
              {{ product }}
            </li>
          </div>
        </details>
      </li>
      <button>
        <li>Careers</li>
      </button>
      <button>
        <li>About</li>
      </button>
      <button class="login-button">
        <li>Login</li>
      </button>
      <button class="register-button">
        <li>Register</li>
      </button>
    </ul>
  </nav>
  <div class="dropbox" id="dropbox">
    <ul class="flex"></ul>
  </div>
  <div class="dropbox" id="dropbox">
    <ul class="flex"></ul>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Dropbox",
  data() {
    return {
      features: [
        "Todo List",
        "Calendar",
        "Reminders",
        "Planning",
      ] as Array<String>,
      icons: [
        {
          icon: "icon-todo.svg",
        },
        {
          icon: "icon-calendar.svg",
        },
        {
          icon: "icon-reminders.svg",
        },
        {
          icon: "icon-planning.svg",
        },
      ] as any,
      company: ["History", "Our Team", "Blog"] as Array<String>,
    };
  },
  mounted() {
    this.company;
    this.features;
    this.icons;
  },
});
</script>

<style scoped>
.logo {
  max-height: 50px;
  height: 3vh;
  min-height: 30px;
}
.flex {
  display: flex;
  gap: var(--gap, 2em);
}

button {
  border: 0;
  background-color: transparent;
}

button {
  font-family: "Epilogue", sans-serif;
  color: hsl(var(--gray));
}

button:hover,
button:focus {
  cursor: pointer;
  color: hsl(var(--black));
}

li {
  font-family: "Epilogue", sans-serif;
  color: hsl(var(--gray));
}

li:hover,
li:focus {
  cursor: pointer;
  color: hsl(var(--black));
}

.register-button {
  border: 2px solid hsl(var(--gray));
  border-radius: 15px;
}

.register-button:hover,
.register-button:focus {
  border: 2px solid hsl(var(--black));
}

@media (min-width: 45em) {
  .flex {
    flex-direction: row;
  }

  .card {
    position: absolute;
  }

  button {
    padding: 0.5em 1em;
  }

  nav {
    padding: 1em 2em;
  }

  ul {
    align-items: center;
    flex-direction: column;
  }
  .login-button {
    margin-left: auto;
  }
}
</style>