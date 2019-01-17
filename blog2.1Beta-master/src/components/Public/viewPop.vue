<template>
    <div class="viewPop" draggable="true">
      <textarea disabled="true" class="text_sure_select">{{text}}</textarea>
      <!-- close -->
      <i class="" @click="closeViewPop()">close</i>
    </div>
</template>

<script>
export default {
  props: ['text'],
  data () {
    return {

    }
  },
  methods: {
    closeViewPop () {
      this.$store.dispatch('set_viewPopShow_state', false)
    }
  },
}
</script>

<style scope>
.viewPop {
  position: fixed;
  left: 15vw;
  width: 50%;
  min-width: 500px;
  height:60%;
  min-height: 300px;
  border: 2px solid #bb7570;
  border-radius: 4px;
  background-color: #113236;
  padding-top: 2em;
}
.viewPop> textarea {
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0);
  border: 0;
  color: #f1f2f1;
  resize: none;
  padding: 11px;
}
.viewPop> i {
  position: absolute;
  right:0;
  top:0;
  display: block;
  background-color: #B0B6B6;
  font-style: normal;
  color: #113236;
  border-radius: 0 0 0 4px;
  padding: 0 1em;
  cursor: pointer;
}
</style>
