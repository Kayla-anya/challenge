<script>
    import Scroller from "./Scroller.svelte";
    import ArticleText from "../lib/ArticleText.svelte";
</script>

<div>
    <Scroller layout="right">
        {#snippet sticky()}
            <img class="duck-img" src="Hat.png" alt="Title" />
        {/snippet}

        {#snippet scrolly()}
            <ArticleText>
                <strong>
                    "There are some states in the United States of America which has a lot more
    Degrees attained by certain races and ethnicity!
                </strong>
            </ArticleText>

            <ArticleText>Based on a chart that shows Undergraduate Employment Rates by Race/Ethnicity by BWDC
                <strong>Asian American</strong> students have the highest rate of employment
                at 6.9 %.</ArticleText>
            <ArticleText>Followed by <strong>African American</strong> students at 6.1 %.</ArticleText>
            <ArticleText>Now looking at a bachelor degree or higher, Asian Americans make up the vast majority at 62.9 %</ArticleText>
            <ArticleText>Asian Americans have the highest rates of higher education in the U.S. and often experience higher income levels and business ownership rates. This might suggest that education is the key to building wealth.

However, when we look at Black Americans with similar education levels, their wealth outcomes are consistently lower. Data from the BWDC shows that in many counties, even with a strong Black college-educated population, homeownership, income, and business ownership rates remain disproportionately low.

This tells us that education matters — but it doesn't fully close the racial wealth gap. Structural barriers like discrimination in hiring, wage gaps, access to capital, and historic inequity continue to block wealth-building even for highly educated Black Americans</ArticleText>
        {/snippet}
    </Scroller>
</div>

<style>
    .duck-img {
        width: 100%;
        margin: 0px auto;
    }
</style>