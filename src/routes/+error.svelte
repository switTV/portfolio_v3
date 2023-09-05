<script lang="ts">
    import { page } from '$app/stores';
</script>

<style>
    .error_container {
        height: 90vh;

        display: flex;
        align-items: center;
    }
    
    .error_container h2 {
        margin-bottom: 0px;
    }

    .error_container p {
        font-family: Montserrat, sans-serif;
        font-size: 20px;
        color: #1768AC;
    }
</style>

<!-- markup (zero or more items) goes here -->
<div class="error_container">
    <div class="error_content">
        <h2>{$page.status} Error</h2>
        <p>{$page.error?.message}</p>
    </div>
</div>