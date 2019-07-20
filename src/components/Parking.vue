<template>
<div id="navbar">
    <b-navbar toggleable="sm" class="b-navbar" fixed="top" type="dark" is-boxed>
        <b-navbar-brand href="#" class="brand"><img src="@/assets/itq_blanco.png">
        </b-navbar-brand>
    </b-navbar>
</div>
</template>
<style scoped>
.b-navbar
{
    background-color: #000000e3;
    padding-bottom: 0;
}
.drop
{
    padding-top: 20px;          
}
.icon1
{
    margin-top: 30px;
}
.icon2
{
    margin-top: 28px;
    margin-left: 15px;
    margin-right: 30px;
}
.brand
{
    margin-left: 5%;
}
</style>
<script>
import {Slide} from 'vue-burger-menu'

    export default
    {
        components:
        {
            Slide
        }
    }

</script>
