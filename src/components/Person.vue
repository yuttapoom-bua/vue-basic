<template>
    <Card>
        <template v-slot:card-header>
        <h1>ชื่อ {{name}}</h1>
        </template>
        <template v-slot:card-content>
            <p></p>
            <p>เงินเดือน {{salary}} บาท</p>
            <p>ตำแหน่งงาน {{department}} เพศ {{gender}}</p>
            <p>ทักษะด้านภาษา {{skill}}</p>
        </template>
    </Card>
</template>

<script>
import Card from './Card.vue'
export default {
    name: "Person",
    components: { Card },
    props: {
        name: {
            type: String,
            required: true
        },
        salary: {
            type: Number,
            default: 0
        },
        department: {
            type: String
        },
        gender: {
            type: String
        },
        skill: {
            type: Array
        },
        inVisible: {
            type: Boolean
        }
    }
}
</script>

<style scoped>

    button{
        margin: 1rem 0;
        font-size: 1.25 rem;
        padding: 0.5rem;
        color: #000;
    }

    .fade-enter-from{
        opacity: 0;
    }
    .fade-enter-active{
        transition: all 0.5s  linear;
    }
</style>

