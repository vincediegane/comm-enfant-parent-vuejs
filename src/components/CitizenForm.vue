<template>
    <div>
        <form @submit.prevent="addCitizen">
            <table align="center">
                <tr>
                    <td>
                        <div>
                            <label for="id">ID : </label>
                            <input type="text" v-model="citizen.id" />
                        </div>
                    </td>
                </tr>
                <tr>
                    <td>
                        <div>
                            <label for="name">NAME : </label>
                            <input type="text" v-model="citizen.name" />
                        </div>
                    </td>
                </tr>
                <tr>
                    <td>
                        <div>
                            <label for="id">AGE</label>
                            <input type="text" v-model="citizen.age" />
                        </div>
                    </td>
                </tr>
            </table>
        </form>
    </div>
</template>

<script>
export default {
    data(){
        return{
            citizen: {
                id: "",
                name: "",
                age: ""
            }
        }
    },
    methods: {
        
    }
}
</script>

<style>

</style>
