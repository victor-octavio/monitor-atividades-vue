<template>
    <section class="py-2">
        <strong class="text-white">
            {{tempoDecorrido}}
        </strong>
    </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
   name: 'CronometroItem',
   props: {
    tempoEmSegundos:{
        type: Number,
        default: 0
    }
   },
   computed: {
    tempoDecorrido() : string {
            return new Date(this.tempoEmSegundos * 1000).toISOString().substr(11,8)
        }
   }

})
</script>

<style>

</style>