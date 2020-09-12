<template>
  <header>
      <h1>{{ propsdata }}</h1>
      <button v-on:click="sendEvent">send</button>
  </header>
</template>

<script>
export default {
    props: ['propsdata'],
    methods: {
        sendEvent: function(){
            this.$emit('renew')
            //상위 컴포넌트 (App.vue)에게 renew라는 emit 이벤트를 올려주게 된다 
            // 받는곳은 해당 컴포넌트를 받게되는 'app-header'태그에서 받게되므로
            // 해당 태그에서 v-on:renew=""를 사용하여 이벤트 조절 가능
        }
    }

}
</script>

<style>

</style>