<template>
  <form class="card" @submit.prevent="onSubmit">
    <h1>Войти в систему</h1>

    <div :class="['form-control', {invalid : eError }]">
      <label for="email">Email</label>
      <input type="email" id="email" v-model="email" @blur="eBlur">
      <small v-if="eError">{{ eError }}</small>
    </div>

    <div :class="['form-control', {invalid : pError }]">
      <label for="password">Password</label>
      <input type="password" id="password" v-model="password" @blur="pBlur">
      <small v-if="pError">{{ pError }}</small>
    </div>

    <button class="btn primary" type="submit" :disabled="isSubmitting || isTooManyAttempts">Войти</button>
    <button class="btn primary" @click.prevent="isHelpOpen = !isHelpOpen">Подсказка</button>
    <div class="pt-1 text" v-if="isHelpOpen">
      <div>Mail: admin1@i.ua</div>
      <div>Pass: admin1</div>
    </div>
    <div class="text-danger" v-if="isTooManyAttempts">Вы слишком часто пытаетесь войти. Попробуйте позже.</div>
  </form>
</template>

<script>
import {useRoute} from "vue-router";
import {useStore} from "vuex";
import {error} from "../utils/error";
import {useLoginForm} from "../use/login-form";
import {ref} from "vue";

export default {


  setup() {
    const route = useRoute()
    const store = useStore()
    const isHelpOpen = ref(false)

    if (route.query.message) {
      store.dispatch('setMessage', {
        value: error(route.query.message),
        type: 'warning'
      })
    }
    return {
      ...useLoginForm(),
      isHelpOpen
    }
  }
}
</script>

<style scoped>

</style>