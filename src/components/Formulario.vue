<script setup>
    const props = defineProps(['cadastraTarefa', 'tarefaTemp', 'trocarFiltro', 'editaTarefaTemp']);
</script>


<template>
    <form @submit.prevent="props.cadastraTarefa">
        <div class="row">
            <div class="col">
                <input :value="props.tarefaTemp" @change="props.editaTarefaTemp" required
                    type="text" placeholder="Digite aqui a descrição da tarefa" class=form-control>
            </div>
            <div class="col-md-2">
                <button type="submit" class="btn btn-primary">Cadastrar</button>
            </div>

            <div class="col-md-4">
                <select @change="props.trocarFiltro" class="form-control">
                    <option class="text-center" value="todas">Todas tarefas</option>
                    <option class="text-center" value="pendentes">Pendentes</option>
                    <option class="text-center" value="finalizadas">Finalizadas</option>
                </select>
            </div>
        </div>
    </form>
</template>