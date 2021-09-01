<template>
  <div class="h-16 w-100 flex text-black-500 bg-white rounded-xl border border-black cursor-pointer" @click="goto()">
  <p class="w-2/3 justify-center m-auto">{{name}}</p>
  <img  class="w-1/3 h-1/3 m-auto justify-right" v-bind:src="require(`../assets/logos/${logo}`)" />
</div>
</template>

<script lang="ts">
import { Options, Vue, computed } from "vue-class-component";
import {Prop} from "vue-property-decorator"
@Options({name: "button-logo"})
export default class ButtonLogo extends Vue {
    
    @Prop({
        type: String,
        default: "No message set",
    }) readonly name: string

    @Prop({
        default: "No logo set",
        required: true
    }) readonly logo: any

    @Prop({
        default: "home",
        required:true,
    }) readonly route: string

    goto(){
        this.$router.push(this.route)
    }
}
</script>
