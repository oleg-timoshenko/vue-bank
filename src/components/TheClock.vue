<!--<template>-->
<!--  <div class="card">-->
<!--    <div>-->
<!--      <button class="btn danger" @click="resetTim">Сброс</button>-->
<!--      <button class="btn primary" @click="pauseTim">Пауза</button>-->
<!--      {{ myHour }} : {{ myMin }} : {{ mySec }} : {{ myMinSec }}-->
<!--    </div>-->

<!--  </div>-->
<!--</template>-->

<!--<script>-->
<!--export default {-->
<!--  data() {-->
<!--    return {-->
<!--      myHour: 0,-->
<!--      myMin: 0,-->
<!--      mySec: 0,-->
<!--      myMinSec: 0-->
<!--    }-->
<!--  },-->
<!--  methods: {-->
<!--    setMyHour() {-->
<!--      setInterval(() => {-->
<!--        if (this.myHour === 23) {-->
<!--          this.myHour = 0-->
<!--        } else {-->
<!--          return this.myHour += 1-->
<!--        }-->
<!--      }, 360000)-->
<!--    },-->
<!--    setMyMin() {-->
<!--      setInterval(() => {-->
<!--        if (this.myMin === 59) {-->
<!--          this.myMin = 0-->
<!--        } else {-->
<!--          return this.myMin += 1-->
<!--        }-->
<!--      }, 60000)-->
<!--    },-->
<!--    setMySec() {-->
<!--      setInterval(() => {-->
<!--        if (this.mySec === 59) {-->
<!--          this.mySec = 0-->
<!--        } else {-->
<!--          return this.mySec += 1-->
<!--        }-->
<!--      }, 1000)-->
<!--    },-->
<!--    setMyMinSec() {-->
<!--      setInterval(() => {-->
<!--        if (this.myMinSec === 99) {-->
<!--          this.myMinSec = 0-->
<!--        } else {-->
<!--          return this.myMinSec += 1-->
<!--        }-->
<!--      }, 1)-->
<!--    },-->
<!--    resetTim() {-->
<!--      this.myHour = 0-->
<!--      this.myMin = 0-->
<!--      this.mySec = 0-->
<!--      this.myMinSec = 0-->
<!--    },-->
<!--    pauseTim() {-->
<!--      clearInterval(this.setMyMinSec)-->
<!--      clearInterval(this.setMySec)-->
<!--      clearInterval(this.setMyMin)-->
<!--      clearInterval(this.setMyHour)-->
<!--    }-->
<!--  },-->
<!--  mounted() {-->
<!--    this.setMyHour()-->
<!--    this.setMyMin()-->
<!--    this.setMySec()-->
<!--    this.setMyMinSec()-->
<!--  }-->
<!--}-->
<!--</script>-->

<!--<style scoped>-->

<!--</style>-->