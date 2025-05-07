<template>
    <div class="grid-wrapper">
        <div v-for="(spaceMission,index) in spaceMissions" :key="spaceMission.id">
            <SpaceMission :spaceMission = spaceMission />
        </div>
    </div>
</template>

<script>
import SpaceMission from "./SpaceMission.vue";

export default{
    name:"SpaceMissionsList",
    components:{
        SpaceMission
    },
    props:{
        spaceMissions: Array
    }
}
</script>

<style>
.grid-wrapper{
    display: grid;
    grid-template-columns: auto;
    gap:2em;
}
</style>