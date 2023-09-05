<script lang="ts">
    import ContactCard from "./Contact_card.svelte";

    let card_svg1 = '<svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-brand-whatsapp" width="84" height="84" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round" style="color: #03256C"><path stroke="none" d="M0 0h24v24H0z" fill="none"></path><path d="M3 21l1.65 -3.8a9 9 0 1 1 3.4 2.9l-5.05 .9"></path><path d="M9 10a.5 .5 0 0 0 1 0v-1a.5 .5 0 0 0 -1 0v1a5 5 0 0 0 5 5h1a.5 .5 0 0 0 0 -1h-1a.5 .5 0 0 0 0 1"></path></svg>'
    let card_svg2 = '<svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-mail" width="84" height="84" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round" style="color: #03256C"><path stroke="none" d="M0 0h24v24H0z" fill="none"></path><path d="M3 7a2 2 0 0 1 2 -2h14a2 2 0 0 1 2 2v10a2 2 0 0 1 -2 2h-14a2 2 0 0 1 -2 -2v-10z"></path><path d="M3 7l9 6l9 -6"></path></svg>'
    let card_svg3 = '<svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-brand-linkedin" width="84" height="84" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round" style="color: #03256C"><path stroke="none" d="M0 0h24v24H0z" fill="none"></path><path d="M4 4m0 2a2 2 0 0 1 2 -2h12a2 2 0 0 1 2 2v12a2 2 0 0 1 -2 2h-12a2 2 0 0 1 -2 -2z"></path><path d="M8 11l0 5"></path><path d="M8 8l0 .01"></path><path d="M12 16l0 -5"></path><path d="M16 16v-3a2 2 0 0 0 -4 0"></path></svg>'
</script>

<style>
    .Main {
        display: flex;
        width: 100%;
        flex-direction: column;
        height: 90vh;
        justify-content: center;
    }
    .Main_cards_container {
        display: flex;
        flex-wrap: wrap;
        width: 100%;
        justify-content: space-between;
    }
    
    @media screen and (max-width: 1071px) {
        .Main {
            display: flex;
            flex-direction: column;
            height: 90vh;
            justify-content: left;
            margin-top: 20px;

        }
        
        .Main_cards_container {
            display: flex;
            justify-content: left;

        }
    }
</style>

<!-- markup (zero or more items) goes here -->

<div class="Main">
    <h2>Contacto</h2>
    <div class="Main_cards_container">
        <ContactCard card_svg={card_svg1} card_text={"Whatsapp"} card_direction={"#"}></ContactCard>
        <ContactCard card_svg={card_svg2} card_text={"Gmail"} card_direction={"#"}></ContactCard>
        <ContactCard card_svg={card_svg3} card_text={"Linkedin"} card_direction={"#"}></ContactCard>
    </div>
</div>