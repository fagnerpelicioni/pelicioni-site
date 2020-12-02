<template>
  <header class="header">
    <div class="header__logo">
      <span class="header__logo--gray">
        {{ 'fagner' }}
      </span>
      <span class="header__logo--primary">
        {{ 'pelicioni' }}
      </span>
    </div>
    <div class="header__menu">
      <ul class="menu-links">
        <li class="menu-links__link">
          <nuxt-link
            to="/"
            class="primary-link"
          >
            {{ 'sobre' }}
          </nuxt-link>
        </li>
        <li class="menu-links__link">
          <nuxt-link
            to="/skills"
            class="primary-link"
          >
            {{ 'habilidades' }}
          </nuxt-link>
        </li>
        <li class="menu-links__link">
          <nuxt-link
            class="primary-link"
            to="/blog"
          >
            {{ 'blog' }}
          </nuxt-link>
        </li>
      </ul>
      <div class="menu-options">
        <div class="menu-options__language">
          en
        </div>
        <div class="menu-options__theme">
          o
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style lang="scss" scoped>
p {
  font-family: $montserrat;
}
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 100px;

  @media (max-width: 768px) {
    flex-direction: column;
  }

  &__logo {
    flex: 1;
    font-family: $montserrat;

    &--primary {
      color: $primary;
      font-weight: $font-bold;
      margin-left: -.25rem;
    }

    &--gray {
      color: $gray-400;
    }
  }

  &__menu {
    width: 40%;
    display: flex;
    justify-content: space-between;

    @media (max-width: 768px) {
      width: 100%;
    }

    @media (min-width: 1440px) {
      width: 30%;
    }

    @media (min-width: 1920px) {
      width: 25%;
    }

    .menu-links {
      display: flex;
      justify-content: space-between;
      flex: 1;

      &__link {
        text-decoration: none;
        list-style: none;
      }
    }

    .menu-options {
      width: 15%;
      display: flex;
      justify-content: space-around;
      margin-left: 2rem;
    }
  }
}
</style>
