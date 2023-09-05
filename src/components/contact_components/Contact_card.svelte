<script lang="ts">
    import Button from "../utils/Button.svelte";

    export let card_svg:string
    export let card_text:string
    export let card_direction:string
    

    // let button_width = 180
    // let text
</script>

<style>
    .Contact_card {
        width: 33%;
        min-width: 250px;
        max-width: 31%;
        height: 400px;
        border: 2px #03256C solid;
        border-radius: 5px;
        margin-left: 10px;
        margin-right: 10px;
        margin-bottom: 10px;
    }

    .Contact_card .top_section {
        display: flex;
        align-items: center;
        flex-direction: column;
        height: 75%;
        justify-content: center;
    }
    
    .Contact_card .top_section p{
        margin-top: 15px;
    }

    .Contact_card .bottom_section {
        display: flex;
        align-items: center;
        flex-direction: column;
    }
</style>

<!-- markup (zero or more items) goes here -->

<div class="Contact_card">
    <div class="top_section">
        {@html card_svg}
        <p>{card_text}</p>
    </div>
    <div class="bottom_section">
        <Button text_button={"Contactame"} width_button={180} direction_button={card_direction}></Button>
    </div>
</div>