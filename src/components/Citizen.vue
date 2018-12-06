<template>
    <div>
        <h3>Citizen detail</h3>
        <h3><span>Id : {{citizen.id}}</span></h3><br>
        <h3><span>Nom : {{citizen.name}}</span></h3><br>
        <h3><span>Age : {{citizen.age}}</span></h3>
    </div>
</template>

<script>
export default {
    props: ['citizen']
}
</script>

<style>

</style>
