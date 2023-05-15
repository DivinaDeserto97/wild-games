<template>
  <div class="navbar-desktop">
    <!-- navbar desktop -->
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
  <div class="navbar-handy">
    <!-- navbar händy -->
    <nav class="navbar bg-body-tertiary fixed-top bg-dark">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">
          <i class="fa-solid fa-alien-8bit"></i>Wild-Games
        </a>
        <button
          class="navbar-toggler btn btn-light"
          type="button"
          data-bs-toggle="offcanvas"
          data-bs-target="#offcanvasNavbar"
          aria-controls="offcanvasNavbar"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div
          class="offcanvas offcanvas-end"
          tabindex="-1"
          id="offcanvasNavbar"
          aria-labelledby="offcanvasNavbarLabel"
        >
          <div class="offcanvas-header">
            <h5 class="offcanvas-title" id="offcanvasNavbarLabel">
              <i class="fa-solid fa-alien-8bit"></i>Wild-Games
            </h5>
            <button
              type="button"
              class="btn-close btn btn-light"
              data-bs-dismiss="offcanvas"
              aria-label="Close"
            ></button>
          </div>
          <div class="offcanvas-body">
            <ul class="navbar-nav justify-content-end flex-grow-1 pe-3">
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
              <li class="nav-item dropdown">
                <a
                  class="nav-link dropdown-toggle"
                  href="#"
                  role="button"
                  data-bs-toggle="dropdown"
                  aria-expanded="false"
                >
                  Medien
                </a>
                <ul class="dropdown-menu">
                  <li>
                    <a class="dropdown-item" href="#">
                      <i class="fa-brands fa-youtube"></i> Youtoube
                    </a>
                  </li>
                  <li>
                    <a class="dropdown-item" href="https://discord.gg/K5tpBH67">
                      <i class="fa-brands fa-discord"></i> Discorde
                    </a>
                  </li>
                </ul>
              </li>
              <li class="nav-item dropdown" style="display: none;">
                <!--  style="display: none;" -->
                <a
                  class="nav-link dropdown-toggle"
                  href="#"
                  role="button"
                  data-bs-toggle="dropdown"
                  aria-expanded="false"
                >
                  User
                </a>
                <ul class="dropdown-menu">
                  <li>
                    <a class="dropdown-item" href="#">
                      <i class="fa-solid fa-arrow-right"></i>
                      <i class="fa-solid fa-user"></i> Login
                    </a>
                  </li>
                  <li>
                    <a class="dropdown-item" href="#">
                      <i class="fa-solid fa-user-pen"></i> Registreiren
                    </a>
                  </li>
                </ul>
              </li>
              <li class="nav-item dropdown">
                <a
                  class="nav-link dropdown-toggle"
                  href="#"
                  role="button"
                  data-bs-toggle="dropdown"
                  aria-expanded="false"
                >
                  User
                </a>
                <ul class="dropdown-menu">
                  <li>
                    <a class="dropdown-item" href="#">
                      <i class="fa-solid fa-user-slash"></i> Logout
                    </a>
                  </li>
                  <li>
                    <a class="dropdown-item" href="#">
                      <i class="fa-solid fa-user"></i> Account
                    </a>
                  </li>
                </ul>
              </li>
            </ul>
            <form class="d-flex mt-3" role="search">
              <input
                class="form-control me-2"
                type="search"
                placeholder="Search"
                aria-label="Search"
              />
              <button class="btn btn-outline-success" type="submit">
                <i class="fa-solid fa-magnifying-glass"></i>
              </button>
            </form>
            <form class="d-flex mt-3">
              <select
                class="form-select form-select-lg mb-3"
                aria-label=".form-select-lg example"
              >
                <option selected>Langue</option>
                <option value="en">English</option>
                <option value="de">German</option>
              </select>
              <button class="btn btn-outline-success" type="submit">
                <i class="fa-regular fa-language"></i>
              </button>
            </form>
            <form>
              <div class="form-check form-switch">
                <input
                  @click="toggleTheme"
                  class="form-check-input"
                  type="checkbox"
                  role="switch"
                  id="flexSwitchCheckChecked"
                  checked
                />
                <label class="form-check-label" for="flexSwitchCheckChecked"
                  >Dark Light</label
                >
              </div>
            </form>
          </div>
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
      const offcanvas = document.querySelector(".offcanvas");

      if (this.isDark) {
        buttons.forEach((button) => {
          button.classList.remove("btn-light");
          button.classList.add("btn-dark");
        });
        navbar.classList.remove("navbar-light", "bg-light");
        navbar.classList.add("navbar-dark", "bg-dark");
        offcanvas.classList.remove("text-bg-dark");
        offcanvas.classList.add("text-bg-light");
        document.body.classList.remove("bg-light");
        document.body.classList.add("bg-dark");
      } else {
        buttons.forEach((button) => {
          button.classList.remove("btn-dark");
          button.classList.add("btn-light");
        });
        navbar.classList.remove("navbar-dark", "bg-dark");
        navbar.classList.add("navbar-light", "bg-light");
        offcanvas.classList.remove("text-bg-light");
        offcanvas.classList.add("text-bg-dark");
        document.body.classList.remove("bg-dark");
        document.body.classList.add("bg-light");
      }
    },

    toggleTheme() {
      this.isDark = !this.isDark;
    },
  },
};
</script>

<style>
/* Navbar Desktop */
.navbar-desktop {
  display: none; /* Versteckt das Element auf allen Geräten */
}

@media (min-width: 768px) {
  .navbar-desktop {
    display: flex !important; /* Zeigt das Element auf Geräten mit einer Breite von 768px oder mehr an */
  }
}

/* Navbar Händy */
.navbar-handy {
  display: flex; /* Zeigt das Element auf allen Geräten an */
}

@media (min-width: 768px) {
  .navbar-handy {
    display: none; /* Versteckt das Element auf Geräten mit einer Breite von 768px oder mehr */
  }
}
</style>
