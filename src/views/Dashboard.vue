<script setup>
import MiniStatisticsCard from "@/examples/Cards/MiniStatisticsCard.vue";
import GradientLineChart from "@/examples/Charts/GradientLineChart.vue";

</script>
<template>
  <div class="py-4 container-fluid">
    <div class="row">
      <div class="col-lg-12">
        <div class="row">
          <div class="col-lg-3 col-md-6 col-12">
            <mini-statistics-card
              title="Registered users"
              value="298k+"
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
              value="61k+"
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
              value="8k+"
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
                description="2024 - 2025"
                :chart="{
                  labels: [
                    'Aug',
                    'Sep',
                    'Oct',
                    'Nov',
                    'Dec',
                    'Jan',
                    'Feb',
                    'Mar',
                    'Apr',
                  ],
                  datasets: [
                    {
                      label: 'new users',
                      data: [17065, 17165, 17595, 17880, 21350, 35660, 54480, 57720, 60085],
                    },
                  ],
                }"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
