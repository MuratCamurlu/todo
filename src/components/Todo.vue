<template>
  <div class="wrapper">
    <h1 class="header">Todo List</h1>
    <div class="inputDiv">
      <input
        ref="myInput"
        type="text"
        class="todoInput"
        v-model="model"
        placeholder="Enter a new Todo"
      />
      <button class="addTodoBtn">Add Todo</button>
    </div>
    <ul class="ul">
      <li v-for="(item, index) in data" :key="index">
        <span>{{ item }}</span>
        <div class="btnGroup">
          <button class="doneBtn">Done</button>
          <button class="deleteBtn">Delete</button>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: "Todo",
  data() {
    return {
      model: "",
      data: [],
    };
  },
};
</script>
<style scoped>
.wrapper {
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.header {
  color: white;
}
.inputDiv {
  width: 90%;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 0.5rem;
}
.todoInput {
  width: 70%;
  padding: 5px;
  border: none;
  border-radius: 10px;
}
.addTodoBtn {
  border: none;
  padding: 5px;
  border-radius: 5px;
  background-color: green;
  color: white;
  cursor: pointer;
}
.addTodoBtn:hover {
  background-color: navy;
  color: white;
}
.ul {
  width: 85%;
  display: flex;
  flex-direction: column;
  padding: 1rem;
  gap: 1rem;
}
.ul li {
  width: 100%;
  display: flex;
  justify-content: space-between;
  border-radius: 5px;
  padding-left: 1rem;
  background-color: white;
}
.btnGroup {
  display: flex;
  justify-content: center;
  gap: 2px;
}
.deleteBtn {
  background-color: white;
  color: red;
  border: none;
  cursor: pointer;
  border-radius: 5px;
}
.deleteBtn:hover {
  background-color: red;
  color: white;
}
.doneBtn {
  background-color: white;
  color: green;
  cursor: pointer;
  border: none;
  border-radius: 5px;
}
.doneBtn:hover {
  background-color: green;
  color: white;
}
</style>
