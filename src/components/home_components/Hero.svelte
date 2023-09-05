<script lang="ts">
    import img_hero from "../../assets/img-hero.png"
    import Button from "../utils/Button.svelte";

    let mouseX = 0
    let mouseY = 0

    function handleMouseMove(event:any) {
        mouseX = event.clientX
        mouseY = event.clientY
    }

    let widthButton = 0
</script>

<svelte:window bind:innerWidth={widthButton}></svelte:window>

<style>
    .Hero {
        display: grid; 
        grid-auto-columns: 1fr; 
        grid-auto-rows: 1fr; 
        grid-template-columns: 1fr 1fr; 
        grid-template-rows: 1.5fr 0.5fr;
        height: 90vh;
        align-items: center;
        gap: 0px 0px; 
        grid-template-areas: 
          "Hero-left-section Hero-right-section"
          "Hero-bottom-section Hero-bottom-section"; 
    }

    .Hero-left-section { 
        grid-area: Hero-left-section;
    }
    .Hero-right-section {
        grid-area: Hero-right-section;
        display: flex;
        justify-content: end;
    }
    .Hero-bottom-section { 
        grid-area: Hero-bottom-section;
        display: flex;
        justify-content: center;
    }

    .Hero .Hero-left-section .Hero-left-section-text h2{
        font-family: "Montserrat";
        color: #1768AC;
        font-size: 64px;
        margin-bottom: 0;
    }

    .Hero .Hero-right-section .Hero-left-section-img {
        position: relative;
    }

    .Hero .Hero-right-section .Hero-left-section-img .Hero-img {
        width: 300px;
        height: 300px;
        border-radius: 5px;
    }
    .Hero .Hero-right-section .Hero-left-section-img .Hero-img-bg {
        width: 300px;
        height: 300px;
        background-color: #1768AC;
        border-radius: 5px;
        position: absolute;
        z-index: -1;
        top: 20px;
        left: 20px;
        bottom: 20px;
    }

    @media screen and (max-width: 768px) {
        .Hero {
            display: grid; 
            grid-auto-columns: 1fr; 
            grid-auto-rows: 1fr; 
            grid-template-columns: 1fr; 
            grid-template-rows: 1fr 1fr 1fr; 
            gap: 0px 0px; 
            grid-template-areas: 
              "Hero-left-section"
              "Hero_right_section"
              "Hero_bottom_section"; 
        }

        .Hero-left-section { 
            grid-area: Hero-left-section;
            display: flex;
            justify-content: center;
        }
        .Hero-right-section {
            grid-area: Hero_right_section;
            display: block;
        }
        .Hero-bottom-section {
            grid-area: Hero_bottom_section;
            display: flex;
            justify-content: center;
        }

        .Hero .Hero-right-section .Hero-left-section-img .Hero-img-bg {
            display: none;
        }
        
        .Hero .Hero-right-section .Hero-left-section-img .Hero-img {
            background-position: center;
            background-size: cover;
            width: 100%;
        }

        
    }
</style>

<!-- markup (zero or more items) goes here -->

<div class="Hero" on:mousemove={handleMouseMove}>
    <div class="Hero-left-section">
        <div class="Hero-left-section-text">
            <h2>Máximo</h2>
            <p>Desarrollador Frontend</p>
        </div>
    </div>
    <div class="Hero-right-section">
        <div class="Hero-left-section-img">
            <div class="Hero-img" style="background-image: url({img_hero}); transform: translate({mouseX / 50}px, {mouseY / 50}px);"></div>
            <div class="Hero-img-bg" style="transform: translate({mouseX / 30}px, {mouseY / 30}px);"></div>
        </div>
    </div>
    <div class="Hero-bottom-section">
        <Button width_button={widthButton/2.8} text_button={"Ir a proyectos!"} direction_button={"/projects"}></Button>
    </div>
</div>