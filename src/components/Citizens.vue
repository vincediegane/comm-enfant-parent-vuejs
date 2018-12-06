<template>
    <div>
        <table border="1%" align="center">
            <tr>
                <th>id</th>
                <th>nom</th>
                <th>age</th>
            </tr>
            <tr v-for="citizen in citizens" :key="citizen.id" @click="selectedCitizen(citizen)">
                <td><h3>{{citizen.id}}</h3></td>
                <td><h3>{{citizen.name}}</h3></td>
                <td><h3>{{citizen.age}}</h3></td>
            </tr>
        </table>
    </div>
</template>

<script>
export default {
    data(){
        return{
            citizens: [
                {
                    id: 1,
                    name: 'Vincent',
                    age: 26
                },
                {
                    id: 2,
                    name: 'Modou',
                    age: 27
                },
                {
                    id: 3,
                    name: 'Doudou',
                    age: 23
                },
                {
                    id: 4,
                    name: 'Fanta',
                    age: 20
                }
            ]
        }
    },
    methods: {
        selectedCitizen(citizen){
            this.$emit('selected', citizen)
        }
    }
}
</script>

<style>

</style>
