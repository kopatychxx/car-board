<template>
  <div class="menu">
    <img src="../assets/logo.svg" alt="" style="max-width: 135px" />
    <ul class="menu__items">
      <li class="menu__items__item">
        <img src="../assets/menu__items/overview_icon.svg" alt="" /> Overview
      </li>
      <li class="menu__items__item">
        <img src="../assets/menu__items/transactions_icon.svg" alt="" />
        Transactions
      </li>
      <li class="menu__items__item">
        <img src="../assets/menu__items/card_icon.svg" alt="" /> Cards
      </li>
      <li class="menu__items__item">
        <img src="../assets/menu__items/invoices_icon.svg" alt="" /> Invoices
      </li>
      <li class="menu__items__item">
        <img src="../assets/menu__items/goals_icon.svg" alt="" /> Goals
      </li>
      <li class="menu__items__item">
        <img src="../assets/menu__items/settings_icon.svg" alt="" /> Settings
      </li>
    </ul>
    <div class="menu__premium">
      <img src="../assets/premiun__img.svg" alt="" />
      <span>
        Give your money <br />
        awesome space in cloud</span
      >
      <button>Upgrade to premium</button>
    </div>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Menu",
};
</script>

<style scoped>
.menu {
  display: flex;
  flex-direction: column;
  max-width: 250px;
  padding: 50px;
  height: 100vh;
  align-items: center;
  box-shadow: 0px 24px 32px rgba(0, 0, 0, 0.04), 0 16px 24px rgba(0, 0, 0, 0.04),
    0px 4px 8px rgba(0, 0, 0, 0.04), 0px 0px 1px rgba(0, 0, 0, 0.04);
}
.menu__items {
  display: flex;
  flex-direction: column;
  row-gap: 5px;
  margin-top: 80px;
}
.menu__items__item {
  list-style: none;
  display: flex;
  align-items: center;
  column-gap: 10px;
  width: 165px;
  height: 39px;
  border-radius: 4px;
  text-align: center;
  font-size: 14px;
}
.menu__items__item:first-child,
.menu__items__item:hover {
  background: #f0f7ff;
  font-weight: bold;
  color: #197bbd;
}
.menu__premium {
  display: flex;
  flex-direction: column;
  position: absolute;
  bottom: 50px;
  align-items: center;
  text-align: center;
}
.menu__premium img {
  max-width: 70px;
}
.menu__premium span {
  font-size: 12px;
  color: #404040;
}
.menu__premium button {
  width: 163px;
  height: 41px;
  background: #ffc145;
  border-radius: 13px;
  font-size: 11px;
  color: #404040;
}
</style>
