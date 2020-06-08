<template>
  <div>{{parentData}}</div>
</template>
<script>
export default {
  name: 'textCom',
  props: {
    parentData: {
      type: String
    }
  }

}
</script>