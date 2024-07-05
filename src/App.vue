<script setup>
import { ref } from 'vue';

const informacoes = ref({
  nome: '',
  sobrenome: '',
  senha: '',
  confirmSenha: '',
  dataNasc: '',
  endereco: '',
  cidade: '',
  estado: '',
  hobbies: [],
  linguagens: '',
  bio: ''
})


let estados = [
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


const enviar = ref(true)
</script>

<template>
  <main>
    <form class="formulario" v-if="enviar">
      <h1>Seu novo Cadastro</h1>
      <div class="row mb-4">
        <div class="col">
          <div class="form-outline">
            <input type="text" class="form-control" v-model="informacoes.nome" placeholder="Nome" />
          </div>
        </div>

        <div class="col">
          <div class="form-outline">
            <input
              type="text"
              class="form-control"
              v-model="informacoes.sobrenome"
              placeholder="Sobrenome"
            />
          </div>
        </div>
      </div>

      <div class="email">
        <input type="email" class="form-control" v-model="informacoes.email" placeholder="E-mail" />
      </div>

      <div class="senha">
        <input
          type="password"
          class="form-control"
          v-model="informacoes.senha"
          placeholder="Senha"
        />
      </div>

      <div class="confsenha">
        <input
          type="password"
          class="form-control"
          v-model="informacoes.confirmSenha"
          placeholder="Confirme sua senha"
        />
      </div>

      <div  class="dataNas">
        <label for="dataNasc">Data de nascimento:</label>
        <input
          type="date"
          id="dataNasc"
          class="form-control"
          v-model="informacoes.dataNasc"
          placeholder="Data de nascimento"
        />
      </div>

      <div  class="endereco">
        <input
          type="text"
          class="form-control"
          v-model="informacoes.endereco"
          placeholder="Endereço"
        />
      </div>

      <div class="cidade">
        <input type="text" class="form-control" v-model="informacoes.cidade" placeholder="Cidade" />
      </div>

      <div class="estado">
        <label class="form-label" for="estado">Estado:</label>
        <select class="form-select" id="estado" v-model="informacoes.estado">
          <option v-for="estado of estados" :key="estado">{{ estado.name }}</option>
        </select>
      </div>

      <section class="hobbies">
        <p>Seus Hobbies:</p>
        <div class="form-check form-check-inline">
          <input
            class="form-check-input"
            type="checkbox"
            id="Dançar"
            v-model="informacoes.hobbies"
            value="Dançar"
          />
          <label class="Esporte" for="esportes">Dançar</label>
        </div>
        <div class="musica">
          <input
            class="form-check-input"
            type="checkbox"
            id="musica"
            v-model="informacoes.musica"
            value="musica"
          />
          <label class="form-check-label" for="musica">Música</label>
        </div>
        <div class="form-check form-check-inline">
          <input
            class="form-check-input"
            type="checkbox"
            id="leitura"
            v-model="informacoes.leitura"
            value="leitura"
          />
          <label class="form-check-label" for="leitura">Leitura</label>
        </div>
      </section>

      <section class="linguagens">
        <p>Linguagem preferida:</p>
        <div class="linguagens">
          <input
            class="form-check-input"
            type="radio"
            id="js"
            value="js"
            v-model="informacoes.linguagens"
          />
          <label class="form-check-label" for="js">JavaScript</label>
        </div>
        <div class="form-check form-check-inline">
          <input
            class="form-check-input"
            type="radio"
            id="swift"
            value="swift"
            v-model="informacoes.linguagens"
          />
          <label class="form-check-label" for="pyton">Swift</label>
        </div>
        <div class="form-check form-check-inline">
          <input
            class="form-check-input"
            type="radio"
            id="php"
            value="php"
            v-model="informacoes.linguagens"
          />
          <label class="form-check-label" for="php">PHP</label>
        </div>
        <div class="form-check form-check-inline">
          <input
            class="form-check-input"
            type="radio"
            id="c"
            value="c"
            v-model="informacoes.linguagens"
          />
          <label class="form-check-label" for="c">C</label>
        </div>
      </section>

      <div data-mdb-input-init class="form-outline mb-4">
        <textarea
          class="form-control"
          id="form6Example7"
          rows="4"
          placeholder="Biografia"
          v-model="informacoes.bio"
        ></textarea>
      </div>

      <button
        @click="enviar = false"
        data-mdb-ripple-init
        type="button"
        class="btn btn-primary btn-block mb-4"
      >
        
      </button>
    </form>
    <section v-else>
      <div class='infoConf'>
        <h2>Suas informações de cadastro:</h2>
        <p>Nome: {{ informacoes.nome }}</p>
        <p>Sobrenome: {{ informacoes.sobrenome }}</p>
        <p>E-mail: {{ informacoes.email }}</p>
        <p>Senha: {{ informacoes.senha }}</p>
        <p>Endereço: {{ informacoes.endereco }}</p>
        <p>Cidade: {{ informacoes.cidade }}</p>
        <p>Estados: {{ informacoes.estado }}</p>
        <p>Hobbies: {{ informacoes.hobbies }}</p>
        <p>Linguagem favorita: {{ informacoes.linguagens }}</p>
        <p>Biografia: {{ informacoes.bio }}</p>
      </div>

      <button
        @click="enviar = true"
        data-mdb-ripple-init
        type="button"
        class="btn btn-primary btn-block mb-4"
      >
        Voltar
      </button>
    </section>
  </main>
</template>

<style scoped>

.formulario {
  border-radius: 5px;
  background-color: blac
  
}

main {
  margin-left: 50%;
  width: 70%;
}



form {
  margin-top: 10%;
}

</style>