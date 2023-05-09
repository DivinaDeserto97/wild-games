<template>
  <div>
    <nav class="navbar navbar-expand-md">
      <div class="container-fluid">
        <div class="row">
          <a class="navbar-brand" href="#">
            <i class="fa-solid fa-alien-8bit"></i>Wild-Games
          </a>
          <div class="col">
            <form class="d-flex" role="search">
              <input
                class="form-control me-2"
                type="search"
                placeholder="Search"
                aria-label="Search"
              />
              <button class="btn btn-light" type="submit">
                <i class="fa-solid fa-magnifying-glass"></i>
              </button>
            </form>
          </div>

          <div class="col-2">
            <!-- social media -->
            <button class="btn btn-light ms-auto">
              <a class="nav-link" href="#">
                <i class="fa-brands fa-youtube"></i>
              </a>
            </button>
            <button class="btn btn-light ms-auto">
              <a class="nav-link" href="https://discord.gg/K5tpBH67">
                <i class="fa-brands fa-discord"></i>
              </a>
            </button>
          </div>
          <div class="col-2">
            <button class="btn btn-light ms-auto">
              <!-- login -->
              <i class="fa-solid fa-arrow-right"></i>
              <i class="fa-solid fa-user"></i>
            </button>
            <button class="btn btn-light ms-auto">
              <!-- registrieren -->
              <i class="fa-solid fa-user-pen"></i>
            </button>
          </div>
          <div class="col-2" style="display: none">
            <button class="btn btn-light ms-auto">
              <!-- logout -->
              <i class="fa-solid fa-user-slash"></i>
            </button>
            <button class="btn btn-light ms-auto">
              <!-- account -->
              <i class="fa-solid fa-user"></i>
            </button>
          </div>
          <div class="col-2">
            <button class="btn btn-light ms-auto">
              <i class="fa-regular fa-language"></i>
            </button>
            <button @click="toggleTheme" class="btn btn-light ms-auto">
              <i class="fa-solid fa-circle-half-stroke"></i>
            </button>
          </div>
        </div>
        <div class="row">
          <ul class="navbar-nav">
            <li class="nav-item">
              <a class="nav-link" href="#">Welcome</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Games</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">About us</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Contact</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </div>
<!--   <WelcomePadge /> -->
</template>

<script>
/* import WelcomePadge from "./components/WelcomePage.vue"; */

export default {
  data() {
    return {
      isDark: false,
    };
  },
  watch: {
    isDark() {
      this.setTheme();
    },
  },
  mounted() {
    this.setTheme();
  },
  methods: {
    setTheme() {
      const buttons = document.querySelectorAll(".btn");
      const navbar = document.querySelector(".navbar");

      if (this.isDark) {
        buttons.forEach((button) => {
          button.classList.remove("btn-light");
          button.classList.add("btn-dark");
        });
        navbar.classList.remove("navbar-light", "bg-light");
        navbar.classList.add("navbar-dark", "bg-dark");
      } else {
        buttons.forEach((button) => {
          button.classList.remove("btn-dark");
          button.classList.add("btn-light");
        });
        navbar.classList.remove("navbar-dark", "bg-dark");
        navbar.classList.add("navbar-light", "bg-light");
      }
    },
    toggleTheme() {
      this.isDark = !this.isDark;
    },
  },
};
</script>
