<template>
<section>
    <div>
        <p>Meu Conteúdo</p>
        <div>
            <!-- V-model -->
            <input v-model="nome" placeholder="Digite seu nome">
            <p>Seu nome é: {{ nome }}</p>

            <!-- V-click -->
            <button @click="submeterFormulario()">Procurar usuário</button>
            
            <!-- V-if e v-else -->
            <p v-if="url">
                {{ url }}

            </p>
            <p v-else>
                Você ainda não buscou usuários
            </p>
        </div>
    </div>
</section>
</template>

<script>

export default {
    name: 'ContentPage',
    data(){
        return{
            nome: '',
            url: ''
        }
    },
    methods: {
        submeterFormulario(){
            fetch(`https://api.github.com/users/${this.nome}`)
            .then((data) => {
                this.data= data.url
                console.log(data.url);
            });

            
        }
    }
}
</script>

<style>

</style>