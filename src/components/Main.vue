<template>
  <div class="main">
    <div class="left">
      <CardCarousels />
      <History />
    </div>
    <div class="right">
      <Goals />
      <Statistic />
    </div>
  </div>
</template>

<script>
import CardCarousels from "@/components/CardCarousels";
import History from "@/components/History";
import Goals from "@/components/Goals";
import Statistic from "@/components/Statistic";
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Main",
  components: { Statistic, Goals, History, CardCarousels },
};
</script>

<style scoped>
.main {
  display: flex;
  flex-direction: row;
  column-gap: 32px;
  justify-content: space-around;
}
</style>
