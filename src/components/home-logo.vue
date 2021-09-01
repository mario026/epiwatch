<template>
  <div class="h-20 w-100 flex ">
  <img  class="m-auto" src="@/assets/logos/Logo.svg" />
</div>
</template>

<script lang="ts">
import { Options, Vue, computed } from "vue-class-component";
import {Prop} from "vue-property-decorator"
@Options({name: "home-logo"})
export default class HomeLogo extends Vue {

}
</script>
