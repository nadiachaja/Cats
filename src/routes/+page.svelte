<script>
    import { Text } from "$lib/index.js";
    import svelte from "$lib/assets/svelte.png";
</script>

<Text as="h1"></Text>
<a href="https://svelte.dev/docs/svelte/svelte-element">Svelte docs</a>

<div>
    <section>
        <img src={svelte} alt="" height="100" width="250" />
        <Text as="h2"></Text>
        <p>Je kan hiermee kiezen welke html element je wil gebruiken. Zo kan
            je herbruikbare componenten maken.</p>
    </section>

    <section>
        <img src={svelte} alt="" height="100" width="250" />
        <Text as="h2"></Text>
        <p>Je kan hiermee kiezen welke html element je wil gebruiken. Zo kan
            je herbruikbare componenten maken.</p>
    </section>
</div>

<style>

    a{
        display: flex;
        justify-self: center;
        padding: 1em;
        margin: 1em;
        color: black;
        background-color: white;
        border: 3px solid orangered;
        width: fit-content;
        border-radius: .5em;
        text-decoration: none;

        &:hover{
            background-color: orangered;
            color: white;
            border: 3px solid orange;
        }
    }

    
    div {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 1em;
        
        @media (min-width: 768px) {
            display: grid;
            grid-template-columns: max-content max-content;
            justify-content: center;
        }
    }

    section {
        background-color: orange;
        display: flex;
        flex-direction: column;
        gap: 1em;
        width: 20em;
        border-radius: 1em;
    }

    img {
        display: flex;
        align-self: center;
        margin: 1em;
    }

    p{
      margin: 1em;
      text-align: center;
    }
</style>
