<template>
  <SpaceMissionHeader/>
  <SpaceMissionsList :spaceMissions = spaceMissions />
</template>

<script>
import SpaceMissionHeader from "./components/SpaceMissionHeader.vue";
import SpaceMissionsList from "./components/SpaceMissionsList.vue";

export default{
  name:"App",
  components:{
    SpaceMissionHeader,
    SpaceMissionsList
  },
  data(){
    return{
      spaceMissions:[]
    }
  },
  methods:{
    async loadSpaceMissionData(){
      const response = await fetch("https://spacemission-5xr4.onrender.com/api");
      const missionData = await response.json();
      console.log(missionData[0].missions);
      return missionData[0].missions;
    }
  },
  async created(){
    this.spaceMissions = await this.loadSpaceMissionData();
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Lora:ital,wght@0,400..700;1,400..700&display=swap');

  *{
     font-family: "Lora", serif;
  }

</style>
