<template>
  <header>
    <div class="header-left">
      <h1>Weekly sumup</h1>
      <p>Get summary of your weekly online transactions here.</p>
    </div>
    <div class="header-right">
      <a href="#"><img src="../assets/mail-icon.svg" alt="" /></a>
      <a href="#"><img src="../assets/bell-icon.svg" alt="" /></a>
      <div class="header-right__account">
        <img src="../assets/account_photo.svg" alt="" />
        <div class="header-right__account__text">
          <h4>Andrew</h4>
          <p
            style="
              margin: 0;
              font-weight: 400;
              font-size: 14px;
              line-height: 17px;
              color: #aeaeae;
            "
          >
            Admin account
          </p>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Header",
};
</script>

<style scoped>
header {
  padding: 40px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}
h1 {
  font-weight: 600;
  font-size: 43px;
  color: #404040;
}
.header-left p {
  font-weight: 400;
  font-size: 16px;
  color: #aeaeae;
}
.header-right {
  display: flex;
  align-items: center;
  column-gap: 15px;
  /*position: absolute;*/
  /*right: 50px;*/
}
.header-right__account {
  display: flex;
  column-gap: 20px;
  align-items: center;
}
</style>
