<template>
  <div class="newTrasaction" style="display: flex; min-height: 240px">
    <div class="newTrasaction__content">
      <h3>New transaction</h3>
      <div class="newTrasaction__content__persons">
        <v-chip-group mandatory active-class="cyan--text">
          <v-chip
            v-for="tag in tags"
            :key="tag"
            style="
              height: 80px;
              padding: 0;
              background: none;
              border-radius: 50px 50px 20px 20px;
            "
          >
            <div
              class="test"
              style="display: flex; flex-direction: column; align-items: center"
            >
              <img :src="tag.img" alt="" style="width: 60px" />
              <p style="margin: 0">{{ tag.name }}</p>
            </div>
          </v-chip>
        </v-chip-group>
        <div class="newTrasaction__content__send">
          <input
            type="number"
            placeholder="0"
            style="
              width: 175px;
              height: 37px;
              background: #ffffff;
              border: 1px solid #197bbd;
              box-sizing: border-box;
              border-radius: 8px;
              outline: none;
              padding: 10px;
            "
          />
          <v-btn
            style="
              width: 132px;
              height: 37px;
              background: #ffc145;
              border-radius: 14px;
              margin-left: 10px;
              font-weight: 700;
              font-size: 10px;
              color: #404040;
            "
            >Send the transfer</v-btn
          >
        </div>
      </div>
    </div>
    <div class="getGreat">
      <div
        class="h3"
        style="
          font-weight: 600;
          font-size: 20px;
          color: #ffff;
          position: absolute;
          bottom: 80px;
          right: 110px;
        "
      >
        Get great loan!
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "NewTransaction",
  data: () => ({
    tags: [
      {
        img: require("../assets/person-avatar/Ann.png"),
        name: "Ann",
      },
      {
        img: require("../assets/person-avatar/Monica.png"),
        name: "Monica",
      },
      {
        img: require("../assets/person-avatar/John.png"),
        name: "John",
      },
      {
        img: require("../assets/person-avatar/Mike.png"),
        name: "Mike",
      },
      {
        img: require("../assets/person-avatar/Mia.png"),
        name: "Mia",
      },
      {
        img: require("../assets/plus-icon.svg"),
        name: "Add new",
      },
    ],
  }),
};
</script>

<style scoped>
.newTrasaction__content {
  padding: 13px;
  box-shadow: 0px 16px 24px rgba(0, 0, 0, 0.06), 0px 2px 6px rgba(0, 0, 0, 0.04),
    0px 0px 1px rgba(0, 0, 0, 0.04);
  border-radius: 19px;
}
v-chip .v-application .primary--text {
  background-color: #fff !important;
}
.getGreat {
  background-image: url("../assets/bg_getgreat.svg");
  background-size: cover;
  background-repeat: no-repeat;
  width: 100%;
}
</style>
