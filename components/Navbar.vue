<template>
  <header>
    <div class="bg-gradient-to-r from-blue-400 to to-purple-400 w-1/4 h-screen text-black">
      <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class=" text-black">
          <ul class="mx-auto space-x-10 text-2xl ml-5 font-bold">
              <li class="nav-item">
                <nuxt-link exact no-prefetch active-class="active" class="nav-link" to="/">
                  <a class="text-4xl" href=""><h1>CPM система</h1></a>
                </nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link exact no-prefetch active-class="active" class="nav-link" to="/">
                  Складский учёт
                </nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link active-class="active" class="nav-link" to="/about">
                  Маркетинг
                </nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link active-class="active" class="nav-link" to="/history">
                  Сайты и Магазины
                </nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link active-class="active" class="nav-link" to="/contacts">
                  Задачи и Проекты
                </nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link active-class="active" class="nav-link" to="/company">
                  Совместная работа
                </nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link active-class="active" class="nav-link" to="/sales">
                  Компания
                </nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link active-class="active" class="nav-link" to="/acoounting">
                  Автоматизцаия
                </nuxt-link>
              </li>
              <li class="nav-item" v-if="!hasToken">
                <nuxt-link active-class="active" class="nav-link" to="/plan">
                  Приложения
                </nuxt-link>
              </li>
              <li class="nav-item" v-if="!hasToken">
                <nuxt-link active-class="active" class="nav-link" to="/profile">
                  Еще
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
