<template>
  <div class="overflow-x-auto bg-red rounded shadow p-4">
    <h2 class="text-lg font-bold mb-2">Tabela Responsiva</h2>
    <table class="min-w-full text-left border-collapse">
      <thead>
        <tr>
          <th class="p-2 border-b">Nome</th>
          <th class="p-2 border-b">Cargo</th>
          <th class="p-2 border-b">Status</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(item, index) in rows" :key="index">
          <td class="p-2 border-b">{{ item.nome }}</td>
          <td class="p-2 border-b">{{ item.cargo }}</td>
          <td class="p-2 border-b">{{ item.status }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script setup>
const rows = [
  { nome: 'João', cargo: 'Dev', status: 'Ativo' },
  { nome: 'Maria', cargo: 'Designer', status: 'Inativo' }
]
</script>
