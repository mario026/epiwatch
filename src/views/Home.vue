<template>
  <div class="h-auto p-5">
    <div class="h-20 m-4"><HomeLogo/></div>
        <div class="h-96 m-4"><UserDetails /></div>
    <div class="h-16 m-4"><ButtonLogo name="Statistieken" logo="chart.svg" route="statistics" /></div>
    <div class="h-16 m-4">
    <ButtonLogo name="Medicatieschema" logo="calender.svg" route="medical"/></div>
    <div class="h-16 m-4">
        <ButtonLogo name="Tips & adviezen" logo="info.svg" route="info" /></div>

  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import ButtonLogo from "../components/button-logo.vue"
import HomeLogo from "../components/home-logo.vue"
import UserDetails from "../components/details/user-details.vue"

@Options({components:{ButtonLogo, HomeLogo, UserDetails}})
export default class Home extends Vue {}
</script>
