<script>
    import { Splide, SplideSlide } from "@splidejs/svelte-splide";
    import "@splidejs/svelte-splide/css/core";

    import Button from "../utils/Button.svelte";
    import CarrouselCard from "./Carrousel_card.svelte";

    import img_slide1 from "../../assets/HBO_minus.webp";
    import img_slide2 from "../../assets/JCF_sistemas.webp";
    import img_slide3 from "../../assets/Julianismo.webp";

    let text_slide1 = "HBO Minus";
    let text_slide2 = "JCF sistemas";
    let text_slide3 = "Julianismo";

    let direction_slide1 = "https://swittv.github.io/HBO-Minus/";
    let direction_slide2 = "http://jcfsistemas.com/";
    let direction_slide3 = "Julianismo";
</script>

<!-- markup (zero or more items) goes here -->

<div class="Carrousel">
    <h2>Proyectos</h2>

    <Splide
        aria-label="Mis proyectos"
        options={{
            rewind: true,
            perPage: 2,
            gap: "2rem",
            arrows: false,
            autoplay: true,

            breakpoints: {
                940: {
                    perPage: 1,
                },
            },
        }}
    >
        <SplideSlide>
            <CarrouselCard
                direction_slide={direction_slide1}
                img_slide={img_slide1}
                text_slide={text_slide1}
            />
        </SplideSlide>
        <SplideSlide>
            <CarrouselCard
                direction_slide={direction_slide2}
                img_slide={img_slide2}
                text_slide={text_slide2}
            />
        </SplideSlide>
        <SplideSlide>
            <CarrouselCard
                direction_slide={direction_slide3}
                img_slide={img_slide3}
                text_slide={text_slide3}
            />
        </SplideSlide>
    </Splide>
</div>

<style>

    .Carrousel {
        height: 90vh;
        display: flex;
        justify-content: center;

        flex-direction: column;
    }

    
    @media screen and (min-width: 412){
        .Carrousel h2 {
            font-size: 12px;
        }
        
    }
</style>
