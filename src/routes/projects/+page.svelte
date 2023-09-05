<script lang="ts">
    import type { PageData } from '../projects/$types';
    import Carrousel from '../../components/projects_components/Carrousel.svelte';

    export let data: PageData;
</script>

<style>
    .Carrousel_container {
        height: 800px;
        display: flex;
        align-items: center;
    }
</style>

<!-- markup (zero or more items) goes here -->
<Carrousel></Carrousel>