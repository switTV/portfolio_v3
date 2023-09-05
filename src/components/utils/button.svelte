<script lang="ts">
    export let width_button:Number
    export let text_button:string
    export let direction_button:string
</script>

<style>
    .Button_section a{
        border: 3px #03256C solid;
        height: 60px;
        display: block;
        border-radius: 10px;
        
        display: flex;
        align-items: center;
        justify-content: center;
        
        font-family: "Montserrat";
        color: #1768AC;
        text-decoration: none;
        min-width: 220px;
    }
    
    .Button_section a:hover {
        transition: border 0.2s ;
        border: 3px #1282A2 solid;
    }
</style>

<!-- markup (zero or more items) goes here -->

<div class="Button_section">
    <a href="{direction_button}" style="width: {width_button}px;">{text_button}</a>
</div>