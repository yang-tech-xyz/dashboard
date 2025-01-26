<script setup>
import MiniStatisticsCard from "@/examples/Cards/MiniStatisticsCard.vue";
import GradientLineChart from "@/examples/Charts/GradientLineChart.vue";

import AU from "@/assets/img/icons/flags/AU.png";
import BR from "@/assets/img/icons/flags/BR.png";
import HK from "@/assets/img/icons/flags/HK.png";
import IN from "@/assets/img/icons/flags/IN.png";
import MA from "@/assets/img/icons/flags/MA.png";
import RU from "@/assets/img/icons/flags/RU.png";
import SI from "@/assets/img/icons/flags/SI.png";
import UK from "@/assets/img/icons/flags/UK.png";
import US from "@/assets/img/icons/flags/US.png";



const sales = {
  us: {
    country: "United States",
    sales: "55k+",
    value: "14k+",
    bounce: "25.45%",
    flag: US,
  },
  in: {
    country: "India",
    sales: "50k+",
    value: "12k+",
    bounce: "24.00%",
    flag: IN,
  },
  ru: {
    country: "Russia",
    sales: "35k+",
    value: "9k+",
    bounce: "25.71%",
    flag: RU,
  },
  br: {
    country: "Brasil",
    sales: "25k+",
    value: "8k+",
    bounce: "32.00%",
    flag: BR,
  },
  uk: {
    country: "United Kingdom",
    sales: "22k+",
    value: "7k+",
    bounce: "31.82%",
    flag: UK,
  },
  au: {
    country: "Australia",
    sales: "18k+",
    value: "6k+",
    bounce: "33.33%",
    flag: AU,
  },
  ma: {
    country: "Malaysia",
    sales: "17k+",
    value: "5.5k+",
    bounce: "32.35%",
    flag: MA,
  },
  hk: {
    country: "Hong Kong",
    sales: "15k+",
    value: "5k+",
    bounce: "33.33%",
    flag: HK,
  },
  si: {
    country: "Singapore",
    sales: "13k+",
    value: "3.5k+",
    bounce: "26.92%",
    flag: SI,
  },
};
</script>
<template>
  <div class="py-4 container-fluid">
    <div class="row">
      <div class="col-lg-12">
        <div class="row">
          <div class="col-lg-3 col-md-6 col-12">
            <mini-statistics-card
              title="Registered users"
              value="250k+"
              description="<span
                class='text-sm font-weight-bolder text-success'
                >+32%</span> since last month"
              :icon="{
                component: 'ni ni-money-coins',
                background: 'bg-gradient-primary',
                shape: 'rounded-circle',
              }"
            />
          </div>
          <div class="col-lg-3 col-md-6 col-12">
            <mini-statistics-card
              title="Wallet Users"
              value="50k+"
              description="<span
                class='text-sm font-weight-bolder text-success'
                >+37%</span> since last week"
              :icon="{
                component: 'ni ni-world',
                background: 'bg-gradient-danger',
                shape: 'rounded-circle',
              }"
            />
          </div>
          <div class="col-lg-3 col-md-6 col-12">
            <mini-statistics-card
              title="Airdrop Users"
              value="7k+"
              description="<span
                class='text-sm font-weight-bolder text-success'
                >+216%</span> since last week"
              :icon="{
                component: 'ni ni-paper-diploma',
                background: 'bg-gradient-success',
                shape: 'rounded-circle',
              }"
            />
          </div>
          <div class="col-lg-3 col-md-6 col-12">
            <mini-statistics-card
              title="fan token users"
              value="15k+"
              description="<span
                class='text-sm font-weight-bolder text-success'
                >+35%</span> than last month"
              :icon="{
                component: 'ni ni-cart',
                background: 'bg-gradient-warning',
                shape: 'rounded-circle',
              }"
            />
          </div>
        </div>
        <div class="row">
          <div class="col-lg-12 mb-lg">
            <!-- line chart -->
            <div class="card z-index-2">
              <gradient-line-chart
                id="chart-line"
                title="Users Overview"
                description="<i class='fa fa-arrow-up text-success'></i>
      2025"
                :chart="{
                  labels: [
                    'Apr',
                    'May',
                    'Jun',
                    'Jul',
                    'Aug',
                    'Sep',
                    'Oct',
                    'Nov',
                    'Dec',
                    'Jan',
                  ],
                  datasets: [
                    {
                      label: 'new users',
                      data: [5000, 8000, 13000, 21000, 27000, 45000, 59000, 65000, 72000, 85000],
                    },
                  ],
                }"
              />
            </div>
          </div>
        </div>
        <div class="row mt-4">
          <div class="col-lg-12 mb-lg-0 mb-4">
            <div class="card">
              <div class="p-3 pb-0 card-header">
                <div class="d-flex justify-content-between">
                  <h6 class="mb-2">Users by Country</h6>
                </div>
              </div>
              <div class="table-responsive">
                <table class="table align-items-center">
                  <tbody>
                    <tr v-for="(sale, index) in sales" :key="index">
                      <td class="w-30">
                        <div class="px-2 py-1 d-flex align-items-center">
                          <div>
                            <img :src="sale.flag" alt="Country flag" />
                          </div>
                          <div class="ms-4">
                            <p class="mb-0 text-xs font-weight-bold">
                              Country:
                            </p>
                            <h6 class="mb-0 text-sm">{{ sale.country }}</h6>
                          </div>
                        </div>
                      </td>
                      <td>
                        <div class="text-center">
                          <p class="mb-0 text-xs font-weight-bold">Fans:</p>
                          <h6 class="mb-0 text-sm">{{ sale.sales }}</h6>
                        </div>
                      </td>
                      <td>
                        <div class="text-center">
                          <p class="mb-0 text-xs font-weight-bold">Users:</p>
                          <h6 class="mb-0 text-sm">{{ sale.value }}</h6>
                        </div>
                      </td>
                      <td class="text-sm align-middle">
                        <div class="text-center col">
                          <p class="mb-0 text-xs font-weight-bold">Conversion rate:</p>
                          <h6 class="mb-0 text-sm">{{ sale.bounce }}</h6>
                        </div>
                      </td>
                    </tr>
                  </tbody>
                </table>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
