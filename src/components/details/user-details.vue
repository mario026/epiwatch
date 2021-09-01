<template>
  <div class="h-96 w-100 flex flex-col ">
    <div class="w-100 h-10 text-lg flex self-center text-black-500 ">Laatste meting MiRNA:</div>
    <div class="w-100 text-lg flex text-6xl self-center text-black-500">{{MiRNAValue}}</div>
    <div class="flex flex-row m-4">
      <div class="flex w-1/2"><BloodValue type="Hartslag" image="heart.svg"/></div>
      <div class="flex w-1/2"><BloodValue type="Zuurtstof" image="zuurstof.svg"/></div>
    </div>
    <div class="text-sm text-black-500">
      <div class="float-left">Laatste bevestigde aanval: <span>{{day}}</span></div>
      <div class="float-left">Duur: <span class="float-right">{{time}}</span></div>
    </div>
  </div>
</template>

<script lang="ts">
import { Options, Vue, computed } from "vue-class-component";
import BloodValue from "@/components/details/blood-value.vue"
import { Prop } from "vue-property-decorator";
@Options({ name: "user-details", components:{BloodValue}})
export default class UserDetails extends Vue {
    const MiRNAValue = "0.10"
    const day = "Gisteren: 10:21:07"
    const time = "40 seconden"
}
</script>
