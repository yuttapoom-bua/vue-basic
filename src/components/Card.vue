<template>
    <li>
        <img src="https://cdn-icons-png.flaticon.com/512/3237/3237472.png" />
        <hr/>
        <slot name="card-header"></slot>
        <slot name="card-button"></slot>
        <slot name="card-content"></slot>
    </li>
</template>
<script>

</script>

<style scoped>
    li{
        list-style: none;
        margin: 1rem 0;
        font-size: 1.25 rem;
        font-weight: bold;
        background:tan;
        padding: 0.5rem;
        color: #000;
        border-radius: 0.5rem;
    }
    img{
        width: 30px;
        height: 30px;
    }
</style>