<template>
    <div class='amuz-card'>
        <h2 v-if="menuTitle">
            {{ menuTitle }}
        </h2>
        <p v-else class="untitled">
            no title
        </p>
        <ul :style="{'background-color':backbroundColor}">

            <li v-for="menu in menuCount" :key="menu">{{menu}}</li>

        </ul>
    </div>
</template>

<script>
export default {
    props :{
        menuTitle : String,
        menuCount : Number,
        backbroundColor : String,
    },
    components : {

    }
}
</script>

<style>
.amuz-card{
    background:#fff;
    margin:20px 0;
    border:3px solid #eee;
    border-radius:10px;
    padding:20px;
}
.untitled{
    background:#eee; text-align:center;
}
</style>