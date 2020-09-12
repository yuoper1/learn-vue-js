<template>
<!-- 탬플릿에서는 하나의 루트 html 태그만 존재해야한다. -->
  <div>
    <!-- <app-header v-bind:프롭스 속성 이름 ="상위 컴포넌트의 데이터 이름"></app-header> -->
        <app-header 
        v-bind:propsdata ="str"
        v-on:renew="renewStr"></app-header>

    <!-- {{ str }} -->
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
// new Vue({
//     data:{
//       str: 'hi'
//     }
// })
export default {
  name: 'vue',
  data: function(){
    return {
      str: 'Header :)'
    }
  },
  components: {
    'app-header': AppHeader
  },
  methods: {
    renewStr: function(){
      this.str = 'send버튼을 눌렀어!'
    }
  }
}
</script>

<style>

</style>