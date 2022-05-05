<template>
  <nav>
    <ul class="flex" role="list">
      <img src="src/assets/logo.svg" alt="logo" class="logo" />
      <button class="menu-moblie" @click="showDropbox()"></button>
      <li v-show="dropboxDisplay">
        <details>
          <summary>Features</summary>
          <div class="card">
            <ol>
              <li :key="i" v-for="(feature, i) in features">
              <!-- here is the bug -->
                <v-img :src="import(`../assests/${icons[i].icon}`)" />
              <!-- -->
                {{ feature }}
              </li>
            </ol>
          </div>
        </details>
      </li>
      <li v-show="dropboxDisplay">
        <details>
          <summary>Company</summary>
          <div class="card">
            <ol>
              <li :key="i" v-for="(product, i) in company">
                {{ product }}
              </li>
            </ol>
          </div>
        </details>
      </li>
      <li v-show="dropboxDisplay">
        <button>
          Careers
        </button>
      </li>
      <li v-show="dropboxDisplay">
        <button>
          About
        </button>
      </li>
      <li v-show="dropboxDisplay">
        <button class="login-button">
          Login
        </button>
      </li>
      <li v-show="dropboxDisplay">
        <button class="register-button">
          Register
        </button>
      </li>
    </ul>
  </nav>
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
      dropboxDisplay: true as boolean
    };
  },
  methods: {
  showDropbox() {
    this.dropboxDisplay = !this.dropboxDisplay
  }
  },
  mounted() {
    this.company;
    this.features;
    this.icons;
    this.dropboxDisplay;
    this.showDropbox()
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

.menu-moblie {
  display: block;
  position: absolute;
  z-index: 2000;
  right: 1rem;
  top: 1rem;
  background-image: url(../assets/icon-menu.svg);
  background-repeat: no-repeat;
  background-position: center;
  width: 1.5rem;
  aspect-ratio: 1;
  border: 0;
  padding: .5em;
}

.mobile-nav-toggle[open] {
  background-image: url(../assets/icon-close-menu.svg);
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

.card {
  position: relative;
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
    box-shadow: 0px 0px 20px 1px hsl(var(--white));
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

  .menu-moblie {
    display: none;
  }
}
</style>
