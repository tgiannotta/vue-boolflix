<template>
    <header>
        <div class="cerca">
            <input v-model="ricercaUtente" placeholder="Inserisci il nome del film che vuoi cercare " type="text">

            <button @click="$emit('getResult', ricercaUtente)">Cerca</button>
       
        </div>
    </header>
    
</template>


<script>
export default {
    name: 'Header',
    data: function(){
        return {
            ricercaUtente: ''
        }
    }
}
</script>


<style lang="scss" scoped>
    header{
        height: 100px;
        background-color: black;
    
        .cerca{
                text-align: right;
                 line-height: 100px;
                input{
                    height: 30px;
                    width: 300px;
                    margin-right: 30px;
                   
                }
                button{
                    height: 30px;
                    padding: 0 20px;
                    margin-left: 30px;
                    font-size: 15px;
                    border-radius: 10%;
                    margin-right: 50px;
                }
        }
    }
</style>