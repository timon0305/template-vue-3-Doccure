<template>
  <div class="main-wrapper home-fifteen">
    <layoutheader :class="['header-fifteen']" :style="{ background: headerBackground }" />

    <indextenbanner></indextenbanner>
    <indextendoctor></indextendoctor>
    <indextenpatient></indextenpatient>
    <indextenfooter></indextenfooter>
    <cursor />
    <scrolltotop />
  </div>
</template>
<script>
export default {
  data() {
    return {
      headerBackground: "transparent",
    };
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
  beforeUnmount() {
    window.removeEventListener("scroll", this.handleScroll);
  },
  methods: {
    handleScroll() {
      const scroll =
        window.pageYOffset ||
        document.documentElement.scrollTop ||
        document.body.scrollTop;
      // Update the background color based on the scroll position
      this.headerBackground = scroll > 95 ? "#ffffff" : "transparent";
    },
  },
};
</script>
