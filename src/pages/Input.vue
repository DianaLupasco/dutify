<template>
    <div>
        <span> X </span>
        <input type="text" v-form="a1">
            

    </div>
</template>

<script>

export default {
  name: 'Input',
  computed: {
    a1 : {
      get : function(){
        return this.$store.getters.getX
      },
      set : function(val){
        this.$store.commit("setX", val)
      }
    },
    a2 : {
      get : function(){
        return this.$store.getters.getY
      },
      set : function(val){
        this.$store.commit("setY", val)
    }
  }
  }
}
</script>

<style scoped>
</style>
