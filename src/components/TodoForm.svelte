<script>
    let todo = "";
    import {addTodo} from "../stores/todoStore"
    const handleSubmit = () => {
        addTodo(todo)
        todo = ""
        console.log("Submittting")
    }

</script>


<form action="" class="my-6" on:submit|preventDefault={handleSubmit}>
    <div class="flex flex-col text-sm mb-2">
        <label for="" class="font-bold mb-2 text-gray-800">Todo</label>
        <input type="text" bind:value={todo} name="todo" placeholder="What you gonna do??" class="appearance-none shadow-sm border border-gray-200 p-2 focus:outline-none focus:border-gray-500">
    </div>
    <button type="submit" class="bg-blue-500 hover:bg-blue-600 text-white py-2 w-full shadow-sm rounded">Submit</button>
</form>