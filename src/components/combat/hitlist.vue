/* hit list is showing a list of attackable players anyone in gam,e may have this kind of list and they can attack them and earn some points as in mgame views */

<template>
  <div>
    <div class="row blkgry Gp0m0">
      <h3 class="p-3 subtitlefnt">Hit List</h3>
    </div>

    <div class="row no-gutters w-100">
      <ul class="list-group w-100" v-for="(masrc, i) in mafia" :key="i">
        <li class="list-group-item blk50 p-1">
          <div class="row Gp0m0 rounded blkd75 p-2">
            <div class="col-2 Gp0m0">
              <img
                :src="require('../../assets/img/item/' + masrc.mfaimg)"
                class="card-img"
                alt=""
              />
            </div>
            <div class="col-8 px-1">
              <h5 class="text-info titlefnt2 siz25">{{ masrc.mfattl }}</h5>
              <div class="row Gp0m0">
                <div class="col-6 p-0">
                  <h6 class="titlefnt2 siz17">{{ masrc.type }}</h6>
                </div>
                <div class="col-6 pl-2">
                  <h6 class="titlefnt2 siz17">Org: {{ masrc.org }}</h6>
                </div>
                <div class="col-6 p-0">
                  <h6 class="titlefnt2 siz17">Level: {{ masrc.mfalvl }}</h6>
                </div>
                <div class="col-6 pl-2">
                  <h6 class="titlefnt2 siz17">Rank: {{ masrc.rank }}</h6>
                </div>
                <div class="col-12 p-0">
                  <h6 class="titlefnt2 siz17 text-capitalize">
                    bounty by: {{ masrc.bname }}
                  </h6>
                </div>
                <div class="col-12 p-0">
                  <h6 class="titlefnt2 siz15">{{ masrc.btime }}</h6>
                </div>
                <br />
                <br />
                <div class="col-12 p-0">
                  <h6 class="titlefnt2 siz13">
                    bounty for: {{ masrc.bfor }} blood
                  </h6>
                </div>
              </div>
            </div>
            <div class="col-2 p-1">
              <div class="button4 nBtn mt-2 border py-2 rounded">
                <h6 class="text-center">
                  <i class="fab fa-wolf-pack-battalion"></i>
                </h6>
              </div>
            </div>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      mafia: [
        {
          mfaimg: "1.gif",
          mfattl: "Habibur Rahman",
          type: "Modern Mafia",
          org: 15,
          mfalvl: 125,
          rank: 1500,
          bname: "Hassan Shahriar",
          btime: "2 weeks ago",
          bfor: 10000,
        },
        {
          mfaimg: "1.gif",
          mfattl: "Habibur Rahman",
          type: "Modern Mafia",
          org: 15,
          mfalvl: 125,
          rank: 1500,
          bname: "Hassan Shahriar",
          btime: "2 weeks ago",
          bfor: 10000,
        },
        {
          mfaimg: "1.gif",
          mfattl: "Habibur Rahman",
          type: "Modern Mafia",
          org: 15,
          mfalvl: 125,
          rank: 1500,
          bname: "Hassan Shahriar",
          btime: "2 weeks ago",
          bfor: 10000,
        },
        {
          mfaimg: "1.gif",
          mfattl: "Habibur Rahman",
          type: "Modern Mafia",
          org: 15,
          mfalvl: 125,
          rank: 1500,
          bname: "Hassan Shahriar",
          btime: "2 weeks ago",
          bfor: 10000,
        },
        {
          mfaimg: "1.gif",
          mfattl: "Habibur Rahman",
          type: "Modern Mafia",
          org: 15,
          mfalvl: 125,
          rank: 1500,
          bname: "Hassan Shahriar",
          btime: "2 weeks ago",
          bfor: 10000,
        },
        {
          mfaimg: "1.gif",
          mfattl: "Habibur Rahman",
          type: "Modern Mafia",
          org: 15,
          mfalvl: 125,
          rank: 1500,
          bname: "Hassan Shahriar",
          btime: "2 weeks ago",
          bfor: 10000,
        },
        {
          mfaimg: "1.gif",
          mfattl: "Habibur Rahman",
          type: "Modern Mafia",
          org: 15,
          mfalvl: 125,
          rank: 1500,
          bname: "Hassan Shahriar",
          btime: "2 weeks ago",
          bfor: 10000,
        },
        {
          mfaimg: "1.gif",
          mfattl: "Habibur Rahman",
          type: "Modern Mafia",
          org: 15,
          mfalvl: 125,
          rank: 1500,
          bname: "Hassan Shahriar",
          btime: "2 weeks ago",
          bfor: 10000,
        },
      ],
    };
  },
};
</script>