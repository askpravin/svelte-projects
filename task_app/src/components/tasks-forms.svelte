<script lang="ts">
  let newTask = $state("");
  function formSubmitted(e: SubmitEvent) {
    e.preventDefault();
    console.log(newTask);
    console.log("Form submitted");
  }
</script>

<form onsubmit={formSubmitted}>
  <label for="">
    <input
      type="text"
      placeholder="Task name"
      name="newTask"
      bind:value={newTask}
    />
    <div class="button-container"><button>Add Task</button></div>
  </label>
</form>

<style>
  .button-container {
    display: flex;
    justify-content: end;
  }
</style>
