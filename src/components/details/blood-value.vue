<template>
  <div class="flex flex-col">
    <div class="text-2xl ">{{type}}</div>
    <div class="text-xl">{{value}}</div>
    <img class="h-4" v-bind:src="require(`@/assets/logos/${image}`)">
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import { Prop } from "vue-property-decorator";
@Options({ name: "blood-value" })
export default class BloodValue extends Vue {

        @Prop({
        type: String,
        default: "No message set",
    }) readonly type: string

    @Prop({
        default: "No message set",
    }) readonly image: any

     value = 99
}
</script>
