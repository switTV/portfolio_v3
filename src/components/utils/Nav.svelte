<script lang="ts">
    let x:number;

    import BarsMenu from "./Bars_menu.svelte";
</script>

<svelte:window bind:innerWidth={x} />

<!-- markup (zero or more items) goes here -->

<div class="Header">
    
    {#if x >= 680}
        <div class="Header-left-section">
            <a href="/home">About Me</a>
            <a href="/projects">Proyectos</a>
        </div>
        <div class="Header-center-section">
            <h1>M</h1>
        </div>
        <div class="Header-right-section">
            <a href="/contact">Contacto</a>
        </div>
        
    {:else}
        <h1>M</h1>
        <BarsMenu></BarsMenu>
    {/if}
</div>

<style>
    .Header {
        display: flex;
        justify-content: space-between;
        height: 10vh;
        align-items: center;
    }

    .Header a {
        color: #1768AC;
        font-family: "Montserrat";
        text-decoration: none;
    }
    
    .Header h1{
        color: #1282A2;
        font-family: Montserrat, sans-serif;
        font-size: 40px;
        
    }

    .Header .Header-left-section a{
        margin-right: 30px;
    }
</style>
