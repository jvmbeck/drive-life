<template>
  <TesteDesktop v-if="desktop"></TesteDesktop>

  <TesteMobile v-if="mobile"></TesteMobile>
</template>

<script>
import TesteDesktop from "src/components/TesteDesktop.vue";
import TesteMobile from "src/components/TesteMobile.vue";

export default {
  name: "TestePage",

  components: {
    TesteDesktop,
    TesteMobile,
  },
  data() {
    return {
      desktop: true,
      mobile: false,
    };
  },

  created() {
    if (window.innerWidth < 1000) {
      this.desktop = false;
      this.mobile = true;
    }
  },
};
</script>
