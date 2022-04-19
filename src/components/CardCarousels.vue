<template>
  <div
    class="cards"
    style="
      display: flex;
      flex-direction: column;
      justify-content: center;
      padding-top: 20px;
    "
  >
    <h3
      style="
        margin: 10px 26px;
        font-weight: 600;
        font-size: 20px;
        line-height: 25px;
        color: #404040;
      "
    >
      Cards
    </h3>
    <v-carousel hide-delimiters height="360px">
      <template v-slot:prev="{ on, attrs }">
        <div style="background: white">
          <v-btn
            color="white"
            v-bind="attrs"
            v-on="on"
            elevation="0"
            style="max-width: 5px !important"
            ><img src="../assets/left.svg" alt=""
          /></v-btn>
        </div>
      </template>
      <template v-slot:next="{ on, attrs }">
        <div style="background: white; position: absolute; right: 245px">
          <v-btn
            color="white"
            v-bind="attrs"
            v-on="on"
            elevation="0"
            style="max-width: 5px !important"
            ><img src="../assets/right.svg" alt=""
          /></v-btn>
        </div>
      </template>
      <v-carousel-item v-for="(item, i) in items" :key="i">
        <div class="carousel__content">
          <div class="carousel__left">
            <div class="cards__card">
              <div class="cards__card-namecard">
                <h5>cloudcash</h5>
                <p>Premium account</p>
              </div>
              <p class="cardNumber">{{ item.cardNumber }}</p>
              <div class="cards__card__info">
                <div class="cards__card__info-holder">
                  <p>Card Holder</p>
                  <h7>{{ item.cardHolder }}</h7>
                </div>
                <div class="cards__card__info-date">
                  <p>Expire date</p>
                  <h7>{{ item.expireDate }}</h7>
                </div>
              </div>
            </div>
            <div class="limit">
              <v-progress-linear
                background-color="grey lighten-3"
                :value="item.progressValue"
                style="
                  margin-top: 25px;
                  width: 280px;
                  height: 10px;
                  border-radius: 13px;
                "
              ></v-progress-linear>
              <div class="limit__content">
                <p>Weekly payment limit</p>
                <p class="limit__content-number">
                  {{ item.usedPaymentLimit }} / {{ item.paymentLimit }}
                </p>
              </div>
            </div>
          </div>
          <div class="carousel__center"></div>
          <div class="carousel__right">
            <div class="carousel__right-current">
              <h5><span>$</span>{{ item.currentBalance }}</h5>
              <p>Current balance</p>
            </div>
            <div class="carousel__right-income">
              <h8><span>$</span>{{ item.income }}</h8>
              <p>Income</p>
            </div>
            <div class="carousel__right-outcome">
              <h8 style="color: #bb4430"><span>$</span>{{ item.outcome }}</h8>
              <p>Outcome</p>
            </div>
            <div class="carousel__right-deactivate">
              <v-switch
                v-model="statusCard"
                color="primary"
                value="Deacivate card"
                style="position: relative; left: 90px"
              ></v-switch>
              <p>{{ statusCard.toString() }}</p>
            </div>
          </div>
        </div>
      </v-carousel-item>
    </v-carousel>
  </div>
</template>

<script>
export default {
  name: "CardCarousels",
  data: () => ({
    statusCard: ["Deacivate card"],
    items: [
      {
        img: require("../assets/cardbgblue.svg"),
        cardNumber: "5789 **** **** 5555",
        cardHolder: "Kolya",
        expireDate: "12/11",
        usedPaymentLimit: "2323.6",
        paymentLimit: "5000",
        currentBalance: "5000.75",
        income: "3000.50",
        outcome: "2250.60",
        progressValue: 80,
      },
      {
        img: require("../assets/cardbgblue.svg"),
        cardNumber: "5789 **** **** 2847",
        cardHolder: "Yevhenii",
        expireDate: "06/21",
        usedPaymentLimit: "$350.6",
        paymentLimit: "$4000",
        currentBalance: "2850.75",
        income: "1500.50",
        outcome: "350.60",
        progressValue: 8.7,
      },
      {
        img: require("../assets/cardbgblue.svg"),
        cardNumber: "5789 **** **** 2847",
        cardHolder: "Yevhenii",
        expireDate: "06/21",
        usedPaymentLimit: "$350.6",
        paymentLimit: "$4000",
        currentBalance: "2850.75",
        income: "1500.50",
        outcome: "350.60",
        progressValue: 8.7,
      },
    ],
  }),
};
</script>

<style scoped>
.cards {
  width: 596px;
  height: 363px;
  background: linear-gradient(180deg, #ffffff 0%, #ffffff 100%);
  box-shadow: 0px 16px 24px rgba(0, 0, 0, 0.06), 0px 2px 6px rgba(0, 0, 0, 0.04),
    0px 0px 1px rgba(0, 0, 0, 0.04);
  border-radius: 28px;
}
.carousel__content {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 0 35px;
}
.cards__card {
  max-width: 280px;
  background-image: url("../assets/cardbgblue.svg");
  background-size: contain;
  background-repeat: no-repeat;
  padding: 20px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.cards__card-namecard h5 {
  font-weight: 700;
  font-size: 17px;
  color: #ffffff;
}
.cards__card-namecard p {
  font-weight: 700;
  font-size: 10px;
  color: rgba(255, 255, 255, 0.39);
}
.cardNumber {
  font-weight: 500;
  font-size: 22px;
  line-height: 27px;
  color: #ffffff;
  text-align: center;
}
.cards__card__info {
  display: flex;
  column-gap: 50px;
}
.cards__card__info-holder p,
.cards__card__info-date p {
  font-weight: 500;
  font-size: 7px;
  color: #ffffff;
  margin-bottom: 6px !important;
}
.cards__card__info-holder h7,
.cards__card__info-date h7 {
  font-weight: 500;
  font-size: 13px;
  color: #ffffff;
}
.limit__content {
  display: flex;
  justify-content: space-between;
  margin-top: 10px;
}
.limit__content {
  font-weight: 400;
  font-size: 14px;
  color: #aeaeae;
}
.limit__content-number {
  color: #404040;
  font-weight: 600;
}
.carousel__right {
  text-align: right;
}
.carousel__right p {
  font-weight: 400;
  font-size: 14px;
  color: #aeaeae;
  margin: 1px 0px;
}
.carousel__right-current h5 {
  font-weight: 700;
  font-size: 31px;
  color: #197bbd;
}
.carousel__right-current h5 span {
  font-size: 18px;
  margin-right: 5px;
}
.carousel__right-income h8,
.carousel__right-outcome h8 {
  font-weight: 600;
  font-size: 18px;
  color: #439a86;
}
.v-btn:not(.v-btn--round).v-size--default {
  bottom: 80px !important;
  min-width: 10px;
  padding: 0;
}
.v-window__container {
  height: 20px !important;
}
</style>
