<template>
  <header>
    <div class="flex justify-betweens align-items-center bg-gradient-to-r from-blue-400 to to-purple-400 h-20 text-white">
      <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <a class="text-2xl" href="#"><b>CPM Система</b></a>
        <div class="flex justify-between align-items-center text-white">
          <ul class="flex justify-between mx-auto space-x-10 text-xl ml-5 font-bold">
              <li class="nav-item">
                <nuxt-link exact no-prefetch active-class="active" class="nav-link" to="/">
                  Категории
                </nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link active-class="active" class="nav-link" to="/about">
                  Новая запись
                </nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link active-class="active" class="nav-link" to="/history">
                  История
                </nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link active-class="active" class="nav-link" to="/sales">
                  Счет
                </nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link active-class="active" class="nav-link" to="/accounting">
                  Домашняя бухгалтерия
                </nuxt-link>
              </li>
              <li class="nav-item" v-if="!hasToken">
                <nuxt-link active-class="active" class="nav-link" to="/plan">
                  Планирование
                </nuxt-link>
              </li>
              <li class="nav-item" v-if="!hasToken">
                <nuxt-link active-class="active" class="nav-link" to="/profile">
                  Профиль
                </nuxt-link>
              </li>
              <li class="nav-item" v-else>
                <a @click.prevent="logout" class="nav-link" href="#">
                  Logout
                </a>
              </li>
            </ul>
        </div>
      </nav>
    </div>
      </header>
</template>

<script>
export default {
  computed: {
    hasToken() {
      return this.$store.getters.hasToken
    }
  },
  methods: {
    logout() {
      this.$store.dispatch('logout')
      this.$router.push('/login')
    }
  }
}
</script>
