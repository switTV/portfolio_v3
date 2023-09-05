<script>
    import { IconMenu } from "@tabler/icons-svelte";

    let menu_state = true

    function change_menu_state() {
        menu_state = !menu_state
    }
</script>

<style>
    .deactivated{
        display: none;
    }

    .Bars_menu_options {
        background-color: #FEFCFB;

        flex-direction: column;
        height: 100vh;
        width: 200px;
        z-index: 2;

        position: absolute;

        border-radius: 0px 0px 10px 10px;
        border: 2px solid #001F54;
        border-top: none;
        border-right: none;
    }
    
    .Bars_menu_options a{
        height: 33%;
        display: flex;
        align-items: center;
        text-decoration: none;
        
        border-bottom: 2px solid #001F54;
    }

    .Bars_menu_options a:nth-child(3){
        border-bottom: none;
    }
</style>

<!-- al tocar el boton de las barras debe de aparecer un menu voladizo -->

<!-- markup (zero or more items) goes here -->
<div class="Bars_menu">
    <div class="container_icon" on:click={change_menu_state}>
        <IconMenu size={32} color={"#1282A2"} stroke={3}></IconMenu>
    </div>
    <div class="Bars_menu_options" class:deactivated={menu_state} class:activated={!menu_state}>
        <a href="/home">About Me</a>
        <a href="/projects">Proyectos</a>
        <a href="/contact">Contacto</a>
    </div>
</div>