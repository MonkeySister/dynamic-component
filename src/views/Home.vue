<template>
  <div class="home">
    <button @click="changeCom">点击动态切换组件</button>
    <component :is="nowComponent"
               v-bind:parentData="parentData"></component>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import textCom from '@/components/text.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld,
    textCom
  },
  data () {
    return {
      nowComponent: HelloWorld,
      parentData: '来自父组件中的值'
    }
  },
  mounted: {

  },
  created () {

  },
  methods: {
    changeCom () {
      this.nowComponent === HelloWorld ? this.nowComponent = textCom : this.nowComponent = HelloWorld
    }
  }
}
</script>
