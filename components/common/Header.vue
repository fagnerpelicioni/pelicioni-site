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
            {{ $t('menu.about') }}
          </nuxt-link>
        </li>
        <li class="menu-links__link">
          <nuxt-link
            to="/skills"
            class="primary-link"
          >
            {{ $t('menu.skills') }}
          </nuxt-link>
        </li>
        <li class="menu-links__link">
          <nuxt-link
            class="primary-link"
            to="/blog"
          >
            {{ $t('menu.blog') }}
          </nuxt-link>
        </li>
      </ul>
      <div class="menu-options">
        <nuxt-link
          v-if="$i18n.locale !== 'en'"
          class="menu-options__language"
          :to="switchLocalePath('en')"
        >
          <svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
            <g clip-path="url(#clip0)">
              <path d="M6 12C9.31371 12 12 9.31371 12 6C12 2.68629 9.31371 0 6 0C2.68629 0 0 2.68629 0 6C0 9.31371 2.68629 12 6 12Z" fill="#F0F0F0" />
              <path d="M5.73914 5.99992H12C12 5.45837 11.9278 4.93375 11.7933 4.43469H5.73914V5.99992Z" fill="#D80027" />
              <path d="M5.73914 2.86955H11.1194C10.7521 2.2702 10.2824 1.74045 9.7349 1.30432H5.73914V2.86955Z" fill="#D80027" />
              <path d="M6.00004 12C7.41213 12 8.71003 11.512 9.73495 10.6957H2.26514C3.29006 11.512 4.58796 12 6.00004 12Z" fill="#D80027" />
              <path d="M0.88061 9.13041H11.1193C11.4142 8.64926 11.6429 8.12333 11.7933 7.56519H0.206665C0.357063 8.12333 0.585743 8.64926 0.88061 9.13041Z" fill="#D80027" />
              <path d="M2.77931 0.936984H3.32609L2.81749 1.30648L3.01177 1.90434L2.5032 1.53485L1.99462 1.90434L2.16244 1.38785C1.71464 1.76086 1.32216 2.19788 0.998719 2.68481H1.17391L0.850172 2.92001C0.799734 3.00415 0.751359 3.08962 0.705 3.17637L0.859594 3.65217L0.571172 3.44262C0.499477 3.59452 0.433898 3.74984 0.374953 3.90839L0.545273 4.43264H1.17391L0.66532 4.80213L0.859594 5.4L0.351023 5.03051L0.0463828 5.25185C0.0158906 5.49696 0 5.74662 0 6H6C6 2.68631 6 2.29566 6 0C4.81472 0 3.7098 0.343828 2.77931 0.936984ZM3.01177 5.4L2.5032 5.03051L1.99462 5.4L2.1889 4.80213L1.6803 4.43264H2.30895L2.5032 3.83477L2.69745 4.43264H3.32609L2.81749 4.80213L3.01177 5.4ZM2.81749 3.0543L3.01177 3.65217L2.5032 3.28268L1.99462 3.65217L2.1889 3.0543L1.6803 2.68481H2.30895L2.5032 2.08695L2.69745 2.68481H3.32609L2.81749 3.0543ZM5.16394 5.4L4.65537 5.03051L4.1468 5.4L4.34107 4.80213L3.83248 4.43264H4.46112L4.65537 3.83477L4.84962 4.43264H5.47826L4.96966 4.80213L5.16394 5.4ZM4.96966 3.0543L5.16394 3.65217L4.65537 3.28268L4.1468 3.65217L4.34107 3.0543L3.83248 2.68481H4.46112L4.65537 2.08695L4.84962 2.68481H5.47826L4.96966 3.0543ZM4.96966 1.30648L5.16394 1.90434L4.65537 1.53485L4.1468 1.90434L4.34107 1.30648L3.83248 0.936984H4.46112L4.65537 0.339117L4.84962 0.936984H5.47826L4.96966 1.30648Z" fill="#0052B4" />
            </g>
            <defs>
              <clipPath id="clip0">
                <rect width="12" height="12" fill="white" />
              </clipPath>
            </defs>
          </svg>
        </nuxt-link>
        <nuxt-link
          v-if="$i18n.locale !== 'pt'"
          class="menu-options__language"
          :to="switchLocalePath('pt')"
        >
          <svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M6 12C9.31371 12 12 9.31371 12 6C12 2.68629 9.31371 0 6 0C2.68629 0 0 2.68629 0 6C0 9.31371 2.68629 12 6 12Z" fill="#6DA544" />
            <path d="M5.99997 2.34778L10.9565 5.99995L5.99997 9.65212L1.04346 5.99995L5.99997 2.34778Z" fill="#FFDA44" />
            <path d="M6.00003 8.08698C7.15262 8.08698 8.08698 7.15262 8.08698 6.00003C8.08698 4.84744 7.15262 3.91309 6.00003 3.91309C4.84744 3.91309 3.91309 4.84744 3.91309 6.00003C3.91309 7.15262 4.84744 8.08698 6.00003 8.08698Z" fill="#F0F0F0" />
            <path d="M4.9565 5.86963C4.59359 5.86963 4.24337 5.92482 3.9137 6.02725C3.9283 7.16725 4.85652 8.08703 5.99999 8.08703C6.70705 8.08703 7.33152 7.73507 7.70902 7.19715C7.06316 6.38863 6.06938 5.86963 4.9565 5.86963Z" fill="#0052B4" />
            <path d="M8.0482 6.39988C8.07333 6.27041 8.0869 6.13684 8.0869 6.00003C8.0869 4.84742 7.15254 3.91309 5.99995 3.91309C5.13993 3.91309 4.40165 4.43342 4.08215 5.17634C4.36458 5.11782 4.65698 5.087 4.95649 5.087C6.16861 5.08698 7.26515 5.59084 8.0482 6.39988Z" fill="#0052B4" />
          </svg>
        </nuxt-link>
        <v-switch v-model="goDark" @change="theme()" />
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',

  data () {
    return {
      goDark: false
    }
  },

  methods: {
    theme () {
      if (this.goDark === true) {
        this.$emit('dark', this.$vuetify.theme.dark = false)
      } else {
        this.$emit('dark', this.$vuetify.theme.dark = true)
      }
    }
  }
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
      color: var(--v-accent-base);
    }
  }

  &__menu {
    width: 40%;
    display: flex;
    justify-content: space-between;
    align-items: center;

    @media (max-width: 768px) {
      width: 100%;
    }

    @media (min-width: 1440px) {
      width: 30%;
    }

    @media (min-width: 1920px) {
      width: 25%;
    }

    .menu-exact-active {
      color: $primary;
      -webkit-text-stroke: 1px $primary;
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

      &__language {
        margin: auto 1rem ;
        &:focus {
          outline: none;
        }

        svg {
          width: 16px;
          height: 16px;
          transition: .3s;

          &:hover {
            transition: .3s;
            transform: scale(1.3);
          }
        }
      }
    }
  }
}
</style>
