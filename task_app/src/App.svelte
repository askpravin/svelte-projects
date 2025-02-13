<script lang="ts">
  import TasksForms from "./components/tasks-forms.svelte";
  let message = "Tasks App!";
  function addTasks(task: string) {
    console.log(task);
</script>

<main>
  <h1>{message}</h1>
  <TasksForms {addTasks} />
</main>

<style>
  main {
    margin: 1rem auto;
    max-width: 800px;
  }
</style>
