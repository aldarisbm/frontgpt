<script lang="ts">
    // this will be a svelte messaging app component

    import { onMount } from 'svelte';
    import { io } from 'socket.io-client';
    import { writable } from 'svelte/store';

    const socket = io('http://localhost:3000');

    const messages = writable([]);

    let message = '';
    onMount(() => {
        socket.on('message', (message) => {
            messages.update((messages) => [...messages, message]);
        });
    });

    const sendMessage = (message) => {
        socket.emit('message', message);
    };

    export { messages, sendMessage };
</script>

<div>
    <h1>Messages</h1>
    <ul>
        {#each $messages as message}
            <li>{message}</li>
        {/each}
    </ul>
    <input type="text" bind:value={message} />
    <button on:click={() => sendMessage(message)}>Send</button>
</div>
