<template>
  <nav>
    <ul class="flex" role="list">
      <img src="src/assets/logo.svg" alt="logo" class="logo" />
        <li>
         <button @click="showFeaturesDropbox()">
          Features<svg width="10" height="6" xmlns="http://www.w3.org/2000/svg">
            <path
              stroke="#686868"
              stroke-width="1.5"
              fill="none"
              d="m1 1 4 4 4-4"
            />
          </svg>
      </button>
        </li>
        <li>
      <button @click="showCompanyDropbox()">
          Company<svg width="10" height="6" xmlns="http://www.w3.org/2000/svg">
            <path
              stroke="#686868"
              stroke-width="1.5"
              fill="none"
              d="m1 1 4 4 4-4"
            />
          </svg>
      </button>
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
    <ul class="flex">
      <li v-show="!featureDropbox" :key="i" v-for="(feature, i) in features">{{ feature }}</li>
    </ul>
  </div>
  <div class="dropbox" id="dropbox">
    <ul class="flex">
      <li v-show="!companyDropbox" :key="i" v-for="(product, i) in company">{{ product }}</li>
    </ul>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Dropbox",
  data() {
    return {
      featureDropbox: true as boolean,
      companyDropbox: true as boolean,
      features: ["Todo List", "Calendar", "Reminders", "Planning"] as Array<String>,
      company: ["History", "Our Team", "Blog"] as Array<String>,
    };
  },
  methods: {
    showFeaturesDropbox() {
      this.featureDropbox = !this.featureDropbox
    },
    showCompanyDropbox() {
      this.companyDropbox = !this.companyDropbox
    }
  },
  mounted() {
    this.featureDropbox;
    this.companyDropbox
    this.company
    this.features;
    this.showFeaturesDropbox()
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
  align-items: center;
  flex-direction: column;
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

  button {
    padding: 0.5em 1em;
  }

  nav {
    padding: 1em 2em;
  }

  .login-button {
    margin-left: auto;
  }
}
</style>