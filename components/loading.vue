<template>
    <div>
        <div class="imagen"></div>
        <div class="imagen paso2"></div>
        <div class="imagen paso3"></div>
        <div class="imagen paso4"></div>
        <div class="imagen paso5"></div>
    </div>
</template>

<script>
    setInterval(() => {
        const imagen= ""
    }, interval);
</script>

<style>
html,body{

    height: 100%;
}
div{
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
}
.imagen{
    background-image: url(../store/completo.png) ;
    background-repeat: no-repeat;
    height: 80px;
    width: 82px;
    background-position: -0 0;

}
.paso2{
    background-position: -6px;
    
}
.paso3{
    background-position: -92px;
}
.paso4{
    
    background-position: -272px;
}
.paso5{
    background-position: -183px;
    
}
</style>