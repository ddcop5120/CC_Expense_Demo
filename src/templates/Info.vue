<template>
  <div>
    <app-bar></app-bar>
    <p class="text-xs text-right text-primary">同源客服電話：(08)8508-8408</p>
    <div class="flex items-center">
      <SimpleInfo :simpleInfo="info.simpleInfo" />
      <LineChart :dataLabels="true" :showYLabels="false" />
    </div>
    <div class="flex w-full mb-1">
      <section class="w-1/2">
        <AccountInfo :infoTitles="info.accountInfo" class="my-1" />
        <Staging class="mt-4" />
      </section>
      <div class="w-1/2 pl-1">
        <Credits class="my-1" :credits="info.credits" />
        <Points class="my-1" :points="info.points" />
        <Message class="my-1" :message="info.message" />
      </div>
    </div>
    <Detail
      :detailsTitle="accountDetail.detailsTitle"
      :expensesList="accountDetail.expensesList"
    />
  </div>
</template>
<script>
import AppBar from "../components/AppBar.vue";
import AccountInfo from "../components/AccountInfo.vue";
import Credits from "../components/Credits.vue";
import SimpleInfo from "../components/SimpleInfo.vue";
import Points from "../components/Points.vue";
import Message from "../components/Message.vue";
import Staging from "../components/Staging.vue";
import Detail from "../components/Detail.vue";
import LineChart from "../components/Line.vue";
export default {
  props: { info: Object, accountDetail: Object },
  components: {
    AppBar,
    AccountInfo,
    Credits,
    SimpleInfo,
    Points,
    Message,
    Staging,
    Detail,
    LineChart
  },
  data() {
    return {};
  }
};
</script>
