<template>
  <div class="container">
    <navbar />

    <div class="main">
      <board />
      <div class="todo">
        <todo-input />
        <div class="todo-wrapper">
          <todo-item
            :todo="{ todo: 'Some todo text here...', done: false }"
            index="0"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({})
</script>

<style scoped>
.container {
  width: 100%;
  max-width: 768px;
  margin: auto;
  padding-left: 16px;
  padding-right: 16px;
  box-shadow: 0 0.125rem 0.25rem rgba(0, 0, 0, 0.075);
}

.main {
  height: calc(100vh - 80px);
  display: flex;
  flex-direction: column;
  padding-bottom: 32px;
  position: relative;
}

.todo {
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  height: calc(100% - 80px);
}

.todo-wrapper {
  margin-top: 20px;
  flex-grow: 1;
  overflow-y: auto;
}

.todo-wrapper::-webkit-scrollbar-track {
  -webkit-box-shadow: none;
  border-radius: 0;
  background-color: transparent;
}

.todo-wrapper::-webkit-scrollbar {
  width: 8px;
  background-color: transparent;
}

.todo-wrapper::-webkit-scrollbar-thumb {
  border-radius: 10px;
  -webkit-box-shadow: none;
  background-color: transparent;
  transition: all 0.3s ease;
}

.todo-wrapper:hover::-webkit-scrollbar-thumb {
  background-color: #b9d4f1;
}

.todo-wrapper:hover::-webkit-scrollbar {
  background-color: #f1f6f8;
}

@media only screen and (min-width: 768px) {
  .main {
    flex-direction: row;
  }

  .todo {
    margin-left: 16px;
  }
}
</style>
