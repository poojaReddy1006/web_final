<template>
    <div class="mission-container" :style="{backgroundColor: getRandomColor(spaceMission.id)}">
            <div class="mission-image">
                <img :src= spaceMission.imageUrl :alt=spaceMission.name  class="image"/>
            </div>
            <div class="mission-details">
                <h3>{{spaceMission.name }}</h3>
                <p>{{spaceMission.description }}</p>
                <a :href="spaceMission.navigateUrl" target="_blank"><img src="https://img.icons8.com/?size=100&id=86795&format=png&color=000000" alt="Animated space"/> Click Me!</a>
            </div>
    </div>
</template>

<script>
export default{
    name:"SpaceMission",
    props:{
        spaceMission: Object,
    },
    methods:{
        getRandomColor(index) {
            const colors = ['#e2a34d', '#73d2d9','#ff9297'];
            return colors[index % 3];
        }
    }
}
</script>

<style>
 .mission-container{
        display: flex;
        gap: 2em;
        align-items:center;
        width:80%;
        margin:auto;
        border:transparent;
        border-radius: 10px;
        padding:1em;
        margin-bottom: 1em;
    }

    .mission-image .image{
        width:120px;
        height:120px;
        object-fit:cover;
        vertical-align:middle;
        border-radius: 7px;
    }

    a{
        text-decoration: none;
        color:black;
    }

    .mission-details img{
        width: 20px;
        height: 20px;
        vertical-align:middle;
    }

</style>