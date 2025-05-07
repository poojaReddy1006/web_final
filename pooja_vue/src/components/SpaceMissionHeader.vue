<template>
    <header class="header">
        <h1> SPACE MISSIONS <img src="@/assets/launch.gif"/></h1>
    </header>
</template>

<script>
export default{
    name:"SpaceMissionHeader"
}
</script>

<style>
.header{
    text-align:center;
    background: linear-gradient(to left, #f0ad4e, #73d2d9);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.header img{
    width: 30px;
    height: 30px;
}
</style>