<template>
  <div>
    <nav>
      <span class="logo"> Todo list</span>
      <button class="hamberger-button">
        <i class="fas fa-bars"></i>
      </button>
      <button class="add-button">
        <i class="fas fa-plus"></i>
      </button>
      <ul class="nav-list">
        <li class="active">All</li>
        <li>Todo</li>
        <li>Done</li>
      </ul>
    </nav>
    <add-todo-modal ref="addTodoModal" />
    <dropdown-nav ref="dropdownNav" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({})
</script>

<style scoped>
nav {
  position: relative;
  height: 80px;
  min-height: 80px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.nav-list {
  display: flex;
  list-style: none;
  width: 300px;
  justify-content: space-between;
  margin-left: auto;
  display: none;
}

.nav-list li {
  cursor: pointer;
  font-weight: 700;
  font-size: 16px;
  color: rgba(106, 117, 155, 0.3);
}

.nav-list li.active {
  color: #21273d;
}

.logo {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  font-weight: 700;
  font-size: 20px;
  color: #21273d;
}

.add-button,
.hamberger-button {
  border-color: transparent;
  background-color: transparent;
  font-size: 20px;
  color: #6a759b;
  cursor: pointer;
}

@media only screen and (min-width: 768px) {
  nav {
    justify-content: flex-start;
  }
  .add-button,
  .hamberger-button {
    display: none;
  }
  .nav-list {
    display: flex;
  }

  .logo {
    position: relative;
    left: 0;
    transform: translateX(0);
  }
}
</style>
