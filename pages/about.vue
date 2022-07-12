<template class = "td">
    <div class="div1">
        <h1>about page</h1>
    </div>
</template>
<style lang='scss'>
@import '~assets/scss/style1';
@import '~assets/scss/mixins';
h1{
    color: $orange;
}

.div1{
    background: burlywood;
    @include my-mixin-name
}

.td{

    background: blue;
}
</style>
