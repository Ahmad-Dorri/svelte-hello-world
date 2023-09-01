<script lang="ts">
    interface Message {
        title: string;
        content: string;
    }
    const message: Message = {
        title: "hello",
        content: 'good Bye'
    }
    const changeTitle = () => {
        message.title = 'changed'
    }
    $:if(message.title === 'changed'){
        alert('title has changed')
    }
</script>
<h1>{message.title}</h1>
<p>{message.content}</p>

<button on:click={changeTitle} >change the title</button>