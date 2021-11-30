<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />

    <input id="text" value="copy me" />

    <!-- Trigger -->
    <button class="btn" data-clipboard-action="copy" data-clipboard-target="#text">Copy to clipboard</button>
  </div>
</template>

<script>
import ClipboardJS from "clipboard";

export default {
  data: function () {
    return {};
  },
  name: "Home",
  components: {},
  mounted: function () {
    this.setUpClipboard();
  },
  methods: {
    setUpClipboard: function () {
      const button = new ClipboardJS(".btn");
      console.log(button);
    },
  },
};
</script>
