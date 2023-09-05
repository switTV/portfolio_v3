<script lang="ts">
    import type { LayoutData } from "./$types";
    import { fade } from "svelte/transition";
    import Nav from "../components/utils/Nav.svelte";

    export let data: LayoutData;
</script>

<div class="container">
    <div class="main-container">
        <Nav />

        <main>
            {#key data.url}
                <div in:fade={{duration: 200}}>
                    <slot />
                </div>
            {/key}
        </main>
    </div>
</div>

<style>
    :global(*) {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    
    :global(h2) {
        font-family: "Montserrat";
        color: #1768ac;
        font-size: 64px;
        margin-bottom: 30px;
    }
    
    :global(p) {
        font-family: "Montserrat";
        color: #1768ac;
        font-size: 20px;
    }

    :global(h3) {
        font-size: 20px;
        font-family: Montserrat, sans-serif;
        font-weight: 600;
        color: #03256C;
    }

    .container {
        width: 100vw;
        display: flex;
        justify-content: center;
    }

    .main-container {
        width: 80vw;
    }

<<<<<<< HEAD
    :global(h2) {
        font-family: "Montserrat";
        color: #1768ac;
        font-size: 64px;
        margin-bottom: 30px;
    }
    
    @media screen and (max-width: 412px){
        :global(h2) {
            font-family: "Montserrat";
            color: #1768ac;
            font-size: 34px;
            margin-bottom: 30px;
        }

    }
=======
>>>>>>> 77d1bc5058e2c1a8d6efa520dc2b79092205807c
</style>
