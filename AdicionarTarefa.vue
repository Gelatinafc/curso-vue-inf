<template>
 <div class="input-group">
     <!--<input @keyup.enter="adicionarTarefa" v-model="novaTarefa" type="text" />-->
     <entrada-dados @salvar="adicionarTarefa" v-model="novaTarefa" />
   <span class="input-group-btn">
    <button @click="adicionarTarefa" class="btn btn-danger">Adicionar</button> 
   </span>
   </div>

</template>

<script>
import EntradaDados from "@/components/templates/EntradaDados"
export default {
components:{EntradaDados},
data() {
    return{
        novaTarefa:"",
    }
},
methods: {
    adicionarTarefa() {
        this.$emit("adicionarTarefa", this.novaTarefa)
        this.novaTarefa = "";
    },
    associarValor(valor) {
        this.novaTarefa = valor;
    }
}
}
</script>

<style>

</style>