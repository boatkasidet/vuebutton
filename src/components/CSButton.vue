<template>
  <div>
    <b v-on:click="upFunction" class="btn btn-info">ถูกใจ {{lable}}</b>
    <b v-on:click="downFunction" class="btn btn-success ml-3">ไม่ถูกใจ {{lable}}</b>
    <b v-on:click="LoveFunction" class="btn btn-warning ml-3">รักเลย {{lable}}</b>
    <b v-on:click="ResetFunction" class="btn btn-danger ml-3">รีเซ็ท {{lable}}</b>
  </div>
</template>
<script>
export default {
  data: function () {
    return {
      counter: 0,
    };
  },
  props: {
    lable: String,
  },
  methods: {
    upFunction: function () {
      this.counter += 10;
      this.$emit("cc", this.counter);
    },

    downFunction: function () {
      this.counter += -5;
      this.$emit("cc", this.counter);
    },

    LoveFunction: function () {
      this.counter += 10;
      this.$emit("cc", this.counter);
    },

    ResetFunction: function () {
      this.counter = 0;
      this.$emit("cc", this.counter);
    },
  },
};
</script>
<style>
</style>