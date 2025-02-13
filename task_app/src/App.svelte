<script lang="ts">
  import TasksForms from "./components/tasks-forms.svelte";
  let message = "Tasks App!";
</script>

<main>
  <h1>{message}</h1>
  <TasksForms />
</main>

<style>
  main {
    margin: 1rem auto;
    max-width: 800px;
  }
</style>
