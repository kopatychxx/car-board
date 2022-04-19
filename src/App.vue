<template>
  <v-app style="display: flex !important; flex-direction: column !important">
    <Menu />
    <div class="main" style="width: 100%">
      <Header />
      <Main />
    </div>
  </v-app>
</template>

<script>
import Menu from "@/components/Menu";
import Header from "@/components/Header";
import Main from "@/components/Main";

export default {
  name: "App",
  components: { Main, Header, Menu },
  data: () => ({
    //
  }),
};
</script>
<style>
.v-application--wrap {
  display: flex !important;
  flex-direction: row !important;
}
</style>
