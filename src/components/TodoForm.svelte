<script>
    import {addTodo} from "../stores/todoStore.js";
    let todo = '';
    const handleSubmit = () => {
        addTodo(todo);
        todo = '';
        console.log("submitting")
    }

</script>

<form class="my-6" on:submit|preventDefault={handleSubmit}>
    <div class="flex flex-col text-sm mb-2">
        <label class="font-bold mb-2" for="todo">Todo</label>
        <input type="text" bind:value={todo} name="todo" placeholder="Watcha gotta do?" class="appearance-none shadow-sm border border-gray-200 p-2 focus:outline-none focus:border-gray-500 rounded-lg" />
    </div>
    <button type="submit" class="w-full shadow-sm rounded bg-blue-500 hover:bg-blue-600 text-white py-2 px-4">Submit</button>
</form>