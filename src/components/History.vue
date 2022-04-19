<template>
  <div class="history">
    <h3>Transaction history</h3>
    <div class="row-title">
      <p class="column-name">Reciever</p>
      <p class="column-name">Type</p>
      <p class="column-name">Date</p>
      <p class="column-name">Amount</p>
    </div>
    <v-virtual-scroll :items="items" :item-height="50" height="300">
      <template v-slot:default="{ item }">
        <v-list-item style="padding: 0">
          <v-list-item-content>
            <div
              class="v-list-item-content-row"
              style="display: flex; flex-direction: row; align-items: center"
            >
              <div
                class="v-list-item-content-name"
                style="
                  display: flex;
                  column-gap: 5px;
                  align-items: center;
                  width: 180px;
                "
              >
                <img :src="item.img" alt="" />
                <p
                  style="
                    font-weight: 400;
                    font-size: 14px;
                    color: #404040;
                    margin: 0 !important;
                  "
                >
                  {{ item.name }}
                </p>
              </div>
              <div class="v-list-item-content-type" style="width: 160px">
                {{ item.type }}
              </div>
              <div class="v-list-item-content-date" style="width: 155px">
                {{ item.date }}
              </div>
              <div
                class="v-list-item-content-amount"
                style="font-weight: 700; font-size: 14px; color: #404040"
              >
                ${{ item.amount }}
              </div>
            </div>
          </v-list-item-content>
        </v-list-item>
      </template>
    </v-virtual-scroll>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "History",
  data: () => ({
    items: [
      {
        img: require("../assets/shoping.svg"),
        name: "Tesco Market",
        type: "Shopping",
        date: "13 Dec 2020",
        amount: "75.67",
      },
      {
        img: require("../assets/deliver-icon.svg"),
        name: "ElectroMen Market",
        type: "Shopping",
        date: "14 Dec 2020",
        amount: "250.00",
      },
      {
        img: require("../assets/food-icon.svg"),
        name: "Fiorgio Restaurant",
        type: "Food",
        date: "07 Dec 2020",
        amount: "19.50",
      },
      {
        img: require("../assets/sport-icon.svg"),
        name: "John Mathew Kayne",
        type: "Sport",
        date: "6 Dec 2020",
        amount: "350",
      },
      {
        img: require("../assets/person-icon.svg"),
        name: "Ann Marlin",
        type: "Shopping",
        date: "31 Nov 2020",
        amount: "430",
      },
      {
        img: require("../assets/shoping.svg"),
        name: "Tesco Market",
        type: "Shopping",
        date: "13 Dec 2020",
        amount: "75.67",
      },
      {
        img: require("../assets/deliver-icon.svg"),
        name: "ElectroMen Market",
        type: "Shopping",
        date: "14 Dec 2020",
        amount: "250.00",
      },
    ],
  }),
};
</script>

<style scoped>
.history {
  margin-top: 30px;
  width: 596px;
  height: 322px;
  background: #ffffff;
  box-shadow: 0px 16px 24px rgba(0, 0, 0, 0.06), 0px 2px 6px rgba(0, 0, 0, 0.04),
    0px 0px 1px rgba(0, 0, 0, 0.04);
  border-radius: 19px;
  padding: 18px 25px;
  display: flex;
  flex-direction: column;
}
h3 {
  font-weight: 600;
  font-size: 20px;
  color: #404040;
}
.row-title {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin-top: 20px;
  font-weight: 400;
  font-size: 14px;
  color: #aeaeae;
}
.v-list-item-content-type,
.v-list-item-content-date {
  font-weight: 400;
  font-size: 14px;
  line-height: 17px;
  color: #c7c7c7;
}
</style>
