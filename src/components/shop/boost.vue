<template>
  <div>
    <h4 class="hr-sect titlefntnew">Boost Shop</h4>
    <div class="row py-2 text-center Gp0m0" v-for="(sitm, i) in spitm" :key="i">
      <div class="row Gp0m0 tmibg P-2 m-2 bdr2 rounded">
        <div class="col-3">
          <img
            class="mt-3 card-img py-2"
            src="../../assets/img/item/1.gif"
            alt=""
          />
          <!-- <img class="card-img" :src="itmallimg + sitm.img" alt="" /> -->
        </div>
        <div class="col-5 p-0">
          <h3 class="subtitlefnt siz20">{{ sitm.name }}</h3>
          <h4 class="dtlsfnt siz15">{{ sitm.dtls }}</h4>
          <h4 class="dtlsfnt siz15">Cost:{{ cst }} Gold</h4>
        </div>
        <div class="col-4">
          <div
            @click="buy(sitm.id)"
            style="position: relative; top: 30%"
            class="btn text-center siz15 nBtn button4"
          >
            Buy Now
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      itmnm: "",
      itmimg: "",
      itmallimg: "https://mafiasrival.com/item/",
      spitm: [],
      itmid: "",
    };
  },
  beforeCreate() {
    this.$mgo.gt("inventory/game/boost", (rs) => {
      if (rs.status_code === 200) {
        rs.data.forEach((dt) => {
          this.spitm.push(dt);
        });
      }
      console.log(rs);
    });
  },
  methods: {
    beforeOspen() {
      setTimeout(() => {
        window.jq(".v--modal").height(window.jq("#gtmhyHt").outerHeight());
      }, 10);
    },
    buy(id) {
      console.log(id);
      this.$mgo.gt("inventory/add/" + id + "/1", (res) => {
        console.log(res);
      });
    },
  },
};
</script>