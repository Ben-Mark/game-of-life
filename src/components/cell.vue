<template>
  <a @click="toggle" :class="[active ? 'active-style' : 'not-active-style']"  href="#" :title="'index : ['+(this.row-1)+','+(this.col-1)+']\n isAlive : '+this.status"></a>
</template>

<script>
  export default {
    props: ['row','col','active'],
    computed: {
      status: {
        get() {
          return this.active
        },
        set(val) {
          this.$emit('update:active', val)
        }
      }
    },
    mounted(){

    }
    ,
    methods: {
      toggle() {
        this.status = !this.status;
      },
      getTitle(){
        return 'index : ['+(this.row-1)+','+(this.col-1)+']\n isAlive : '+this.status;
      }
    },

  }
</script>

<style >

  .active-style  {
    background-color: #CCC;
    display: flex;
    height: 100%;
    width: 100%;
  }
  .not-active-style {
    background-color: #000000;
    display: flex;
    height: 100%;
    width: 100%;
  }

</style >

