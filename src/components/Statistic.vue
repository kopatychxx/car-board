<template>
  <div class="statistics">
    <h3 style="font-weight: 600; font-size: 20px; color: #404040">
      Outcome Statistics
    </h3>
    <div class="statistics__rows">
      <div class="statistics__rows-shopping rows">
        <img
          src="../assets/shoppingStatistic-icon.svg"
          alt=""
          style="
            shadow: 0px 16px 24px rgba(0, 0, 0, 0.06),
              0px 2px 6px rgba(0, 0, 0, 0.04), 0px 0px 1px rgba(0, 0, 0, 0.04);
          "
        />
        <div
          class="statistics__rows-shopping__content"
          style="
            display: flex;
            flex-direction: column;
            row-gap: 7px;
            padding-top: 20px;
          "
        >
          <v-progress-linear
            color="orange accent-2"
            rounded
            height="10px"
            value="52"
            style="width: 500px"
          ></v-progress-linear>
          <p
            style="
              font-weight: 400;
              font-size: 14px;
              line-height: 17px;
              color: #aeaeae;
            "
          >
            Shopping
          </p>
        </div>
        <span
          style="
            font-weight: 600;
            font-size: 23.9789px;
            line-height: 29px;
            color: #696969;
          "
          >52%</span
        >
      </div>
      <div class="statistics__rows-shopping rows">
        <img
          src="../assets/electonics-icon.svg"
          alt=""
          style="
            box-shadow: 0px 16px 24px rgba(0, 0, 0, 0.06),
              0px 2px 6px rgba(0, 0, 0, 0.04), 0px 0px 1px rgba(0, 0, 0, 0.04);
          "
        />
        <div
          class="statistics__rows-shopping__content"
          style="
            display: flex;
            flex-direction: column;
            row-gap: 7px;
            padding-top: 20px;
          "
        >
          <v-progress-linear
            color="green accent-3"
            rounded
            height="10px"
            value="21"
            style="width: 500px"
          ></v-progress-linear>
          <p
            style="
              font-weight: 400;
              font-size: 14px;
              line-height: 17px;
              color: #aeaeae;
            "
          >
            Electronics
          </p>
        </div>
        <span
          style="
            font-weight: 600;
            font-size: 23.9789px;
            line-height: 29px;
            color: #696969;
          "
          >21%</span
        >
      </div>
      <div class="statistics__rows-shopping rows">
        <img
          src="../assets/travels-icon.svg"
          alt=""
          style="
            box-shadow: 0px 16px 24px rgba(0, 0, 0, 0.06),
              0px 2px 6px rgba(0, 0, 0, 0.04), 0px 0px 1px rgba(0, 0, 0, 0.04);
          "
        />
        <div
          class="statistics__rows-shopping__content"
          style="
            display: flex;
            flex-direction: column;
            row-gap: 7px;
            padding-top: 20px;
          "
        >
          <v-progress-linear
            color="light-blue accent-3"
            rounded
            height="10px"
            value="21"
            style="width: 500px"
          ></v-progress-linear>
          <p
            style="
              font-weight: 400;
              font-size: 14px;
              line-height: 17px;
              color: #aeaeae;
            "
          >
            Travel
          </p>
        </div>
        <span
          style="
            font-weight: 600;
            font-size: 23.9789px;
            line-height: 29px;
            color: #696969;
          "
          >74%</span
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Statistic",
};
</script>

<style scoped>
.rows {
  display: flex;
  flex-direction: row;
  column-gap: 15px;
  align-items: center;
}
</style>
