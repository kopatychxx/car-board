<template>
  <div class="goals">
    <div class="title">
      <h3>Goals</h3>
      <img src="../assets/plus-icon.svg" alt="" />
    </div>
    <div class="slider" style="max-width: 680px">
      <v-slide-group v-model="item" show-arrows>
        <v-slide-item v-for="item in items" :key="item">
          <v-card
            class="ma-4"
            height="168"
            width="158"
            elevation="1"
            style="
              display: flex;
              flex-direction: column;
              justify-content: space-between;
              padding: 13px 24px;
              margin-right: 15px !important;
              background: #ffffff;
              box-shadow: 0px 16px 24px rgba(0, 0, 0, 0.06),
                0px 2px 6px rgba(0, 0, 0, 0.04), 0px 0px 1px rgba(0, 0, 0, 0.04) !important;
              border-radius: 28px;
            "
          >
            <div class="card__number">
              <p
                style="
                  margin: 0;
                  font-weight: 600;
                  font-size: 23.9789px;
                  line-height: 29px;
                  color: #696969;
                "
              >
                {{ item.price }}
              </p>
              <span
                style="
                  font-weight: 400;
                  font-size: 14px;
                  line-height: 17px;
                  color: #aeaeae;
                "
              >
                {{ item.date }}
              </span>
            </div>
            <div class="card_desc">
              <img :src="item.img" alt="" />
              <p
                style="
                  margin: 0;
                  font-weight: 400;
                  font-size: 20px;
                  line-height: 25px;
                  color: #404040;
                "
              >
                {{ item.name }}
              </p>
            </div>
          </v-card>
        </v-slide-item>
      </v-slide-group>
    </div>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Goals",
  data: () => ({
    items: [
      {
        price: "$550",
        date: "12/20/20",
        img: require("../assets/mountain-icon.svg"),
        name: "Holidays",
      },
      {
        price: "$220",
        date: "12/20/20",
        img: require("../assets/renovation-icon.svg"),
        name: "Renovation",
      },
      {
        price: "$820",
        date: "12/20/20",
        img: require("../assets/xbox-icon.svg"),
        name: "Xbox",
      },
      {
        price: "$550",
        date: "12/20/20",
        img: require("../assets/mountain-icon.svg"),
        name: "Holidays",
      },
      {
        price: "$220",
        date: "12/20/20",
        img: require("../assets/renovation-icon.svg"),
        name: "Renovation",
      },
      {
        price: "$820",
        date: "12/20/20",
        img: require("../assets/xbox-icon.svg"),
        name: "Xbox",
      },
    ],
  }),
};
</script>

<style scoped>
.title {
  display: flex;
  align-items: center;
  column-gap: 5px;
}
h3 {
  font-weight: 600;
  font-size: 20px;
  color: #404040;
}
</style>
