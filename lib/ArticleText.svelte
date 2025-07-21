<script>
    let { children } = $props();
</script>

<div class="article-text">
    <p>
        {@render children()}
    </p>
</div>

<style>
    .article-text {
        margin: 90vh auto;
        width: 50%;
        background-color: #64dff0;
        color: #000000;
        border: solid #560a91 3px;
        border-radius: 20px;
        padding: 20px;
        box-shadow: 16px 16px #567ecf;
    }
</style>
