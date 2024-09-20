<template>
    <div>
        <form @submit.prevent="addItem">
            <input type="text" v-model="inputValue">
            <input type="submit" value="Adicionar item na tabela">
        </form>
        <table>
            <tr>
                <td>index</td>
                <td>Key</td>
                
            </tr>
        
            
            

            <tr v-for="(item, index) in itens" :key="index">
                <td>{{ index }}</td>
                <td>{{ item }}</td>
            </tr>
        </table>
        <!---<ul>
            <li v-for="(item, index) in itens" :key="index"> 
                {{ item }}
                {{ index }}
            </li>
        </ul>-->
    </div>
    <br><br><br>
</template>

<script>
export default {
    data(){
        return{
            itens: [],
            inputValue: ''
        }
    },
    methods: {
        addItem(){
            if(this.inputValue){
                this.itens.push(this.inputValue)
                this.inputValue = ''
            }
            
        }

    }
}
</script>

<style>
table, tr, td {
    border: 1px solid black;
    margin: auto;
}

</style>
