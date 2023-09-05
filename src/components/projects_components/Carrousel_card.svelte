<script lang="ts">
    import Button from "../utils/Button.svelte";
    export let img_slide: string;
    export let text_slide: string;
    export let direction_slide: string;

    let width_button = 190;
    let text_button = "Ir!";
    let direction_button = direction_slide;
</script>

<style>
    .Carrousel_card {
        border-radius: 10px;
        border: 2px #2541b2 solid;
        cursor: grab;
    }

    .card_bottom_section {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin: 0px 20px 0px 20px;
        height: 100px;
    }
    
    .card_bottom_section h3 {
        font-size: 20px;
        font-family: Montserrat, sans-serif;
        font-weight: 300;
        color: #03256c;
    }

    .card_top_section {
        height: 300px;
        background-position: 50% 0%;
        background-size: cover;
        border-radius: 8px 8px 0px 0px;
        border-bottom: 2px #2541b2 solid;
    }

    @media screen and (max-width: 768px) {
        /* Agrega aquí los estilos que deseas aplicar para dispositivos móviles */
        .Carrousel_card .card_bottom_section {
            flex-direction: column;
            margin-bottom: 20px;
        }
        
        .Carrousel_card .card_bottom_section h3{
            margin-top: 10px;
        }
    }
</style>
<!-- markup (zero or more items) goes here -->

<div class="Carrousel_card">
    <div class="card_top_section" style="background-image: url({img_slide});" />
    <div class="card_bottom_section">
        <h3>{text_slide}</h3>
        <Button {width_button} {text_button} {direction_button} />
    </div>
</div>

