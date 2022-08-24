<template>
  <div class="sidebar" v-if="sidebar">
    <span class="sidebar-close" @click="close">&times</span>

    <div class="sidebar-content">
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Distinctio iste magni possimus quae quidem! Aliquid delectus dolores officiis quam sit.</p>
    </div>
  </div>
</template>

<script>
import {computed} from "vue";
import {useStore} from "vuex";

export default {
  setup() {
    const store = useStore()

    const sidebar = computed(() => store.state.sidebar)

    return{
      sidebar,
      close: () => store.commit('closeSidebar')
    }
  }
}
</script>

<style scoped>

</style>