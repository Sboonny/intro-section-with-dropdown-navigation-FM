<template>
  <nav>
    <ul class="flex" role="list">
      <img src="src/assets/logo.svg" alt="logo" />
      <button>
        <li>
          Features<svg width="10" height="6" xmlns="http://www.w3.org/2000/svg">
            <path
              stroke="#686868"
              stroke-width="1.5"
              fill="none"
              d="m1 1 4 4 4-4"
            />
          </svg>
        </li>
      </button>
      <button>
        <li>
          Company<svg width="10" height="6" xmlns="http://www.w3.org/2000/svg">
            <path
              stroke="#686868"
              stroke-width="1.5"
              fill="none"
              d="m1 1 4 4 4-4"
            />
          </svg>
        </li>
      </button>
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
  <dialog>
    <ul class="flex">
      <li>Todo List</li>
      <li>Calendar</li>
      <li>Reminders</li>
      <li>Planning</li>
    </ul>
  </dialog>
  <dialog>
    <ul class="flex">
      <li>History</li>
      <li>Our Team</li>
      <li>Blog</li>
    </ul>
  </dialog>
</template>

<style scoped>
.flex {
  display: flex;
  gap: var(--gap, 2em);
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

.login-button {
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