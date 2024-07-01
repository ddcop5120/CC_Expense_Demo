<template>
  <div class="relative h-full">
    <Slogan :info="accountDetail.slogan" class="mt-1" />
    <Terms :terms="accountDetail.term" />
  </div>
</template>
<script>
import Terms from "../components/Terms.vue";
import Slogan from "../components/Slogan.vue";
export default {
  props: { accountDetail: Object },
  components: {
    Terms,
    Slogan
  },
  data() {
    return {};
  }
};
</script>
