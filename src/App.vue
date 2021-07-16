<template>
  <div id="app">
    <child v-bind:msg="ool" v-on:father="showFather"></child>
    {{ show }}
  </div>
</template>

<script>
import child from "./components/Child.vue";
export default {
  name: "app",
  components: {
    child,
  },
  data() {
    return {
      ool: "弄死恁爹 我是你大爷",
      show: "",
    };
  },
  methods: {
    showFather: function (data) {
      this.show = data;
    },
  },
};
</script>
