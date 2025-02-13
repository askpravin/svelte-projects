<script lang="ts">
  import TasksForms from "./components/tasks-forms.svelte";
  let message = "Tasks App!";
  type Task = {
    id: string;
    title: string;
    done: boolean;
  };
  let tasks = $state<Task[]>([]);
  function addTasks(task: string) {
    tasks.push({
      id: crypto.randomUUID(),
      title: task,
      done: false,
    });
  }
</script>

<main>
  <h1>{message}</h1>
  <TasksForms {addTasks} />
  <section>
    {#each tasks as task}
      <article>
        {task.title}
      </article>
    {/each}
  </section>
</main>

<style>
  main {
    margin: 1rem auto;
    max-width: 800px;
  }
</style>
