<template>
  <div>
    <layout-full>
      <template v-slot:content>
        <Info :info="data.InfoData" :accountDetail="data.AccountDetailData" />
        <AccountDetail :accountDetail="data.AccountDetailData" />
        <Bill :bill="data.BillData" /> </template
    ></layout-full>
  </div>
</template>

<script>
import LayoutFull from "../components/layout-full/src/index.vue";
import Info from "../templates/Info.vue";
import AccountDetail from "../templates/AccountDetail.vue";
import Bill from "../components/Bill.vue";
export default {
  props: { data: Object },
  components: {
    Info,
    AccountDetail,
    LayoutFull,
    Bill
  },
  data() {
    return {};
  }
};
</script>
