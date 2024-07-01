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
import testData from "../data/testData.json";
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
      this.data = testData;
    }
  }
};
</script>
