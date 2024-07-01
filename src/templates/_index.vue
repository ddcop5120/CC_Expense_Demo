<template>
  <div>
    <layout-full>
      <template class="font-bold" v-slot:content>
        <PdfView :data="data"/></template
    ></layout-full>
  </div>
</template>

<script>
import "../assets/css/tailwind/tailwind.css";
import LayoutFull from "../components/layout-full/src/index.vue";
import PdfView from "../templates/PdfView.vue";
export default {
  components: { LayoutFull, PdfView },
  data() {
    return {};
  },
  created() {
    this.getData();
  },
  methods: {
    getData() {
      this.data = this.$root;
    }
  }
};
</script>
