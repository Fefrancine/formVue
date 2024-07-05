<script setup>
import { ref } from 'vue';


const informacoes = ref({
  nome: '',
  sobrenome: '',
  senha: '',
  confSenha: '',
  dataNasc: '',
  endereco: '',
  cidade: '',
  estado: '',
  hobbies: '',
  linguagensPro: '',
  biografia: ''
})

let estado = [
  {name : 'Acre(AC)'},
  {name: 'Alagoas(AL)'},
  {name: 'Amapá(AP)'},
  {name: 'Amazonas(AM)'},
  {name: 'Bahia(BA)'},
  {name: 'Ceará(CE)'},
  {name: 'Espírito Santo(ES)'},
  {name: 'Goiás(GO)'},
  {name: 'Maranhão(MA)'},
  {name: 'Mato Grosso(MT)'},
  {name: 'Mato Grosso Do Sul(MS)'},
  {name: 'Minas Gerais(MG)'},
  {name: 'Pará(PA)'},
  {name: 'Paraíba(PB)'},
  {name: 'Paraná(PR)'},
  {name: 'Pernambuco(PE)'},
  {name: 'Piauí(PI)'},
  {name: 'Rio De Janeiro(RJ)'},
  {name: 'Rio Grande Do Norte(RN)'},
  {name: 'Rio Grande Do Sul(RS)'},
  {name: 'Rondônia(RO)'},
  {name: 'Roraima(RR)'},
  {name: 'Santa Catarina(SC)'},
  {name: 'São Paulo(SP)'},
  {name: 'Sergipe(SE)'},
  {name: 'Tocantins(TO)'},
  {name: 'Distrito Federal(DF)'}
]
const enviarInfo = ref(true)
</script>

<template>
  <main>

  </main>
</template>