<script>
    import { fade, fly } from "svelte/transition";
    import Scroller from "./Scroller.svelte";
    

    let duckIsVisible = $state(false);

    const options = {
        threshold: [0.85, 0.95],
    };

    const simpleCallback = (entries, observer) => {
        entries.forEach((entry) => {
            const elem = entry.target;

            if (entry.intersectionRatio >= 0.9) {
                // "active" state
                elem.style.backgroundColor = "#e3ff00";
            } else if (entry.intersectionRatio < 0.9) {
                // "inactive" state
                elem.style.backgroundColor = "#888888";
            }
        });
    };

    const showDuckCallback = (entries, observer) => {
        entries.forEach((entry) => {
            const elem = entry.target;

            if (entry.intersectionRatio >= 0.9) {
                elem.style.backgroundColor = "#e3ff00";
                duckIsVisible = true;
            } else if (entry.intersectionRatio < 0.9) {
                elem.style.backgroundColor = "#888888";
            }
        });
    };

    const removeDuckCallback = (entries, observer) => {
        entries.forEach((entry) => {
            const elem = entry.target;

            if (entry.intersectionRatio >= 0.9) {
                elem.style.backgroundColor = "#e3ff00";
                duckIsVisible = false;
            } else if (entry.intersectionRatio < 0.9) {
                elem.style.backgroundColor = "#888888";
            }
        });
    };
</script>

<div>
    <Scroller layout="left">
        {#snippet sticky()}
            <div>
                {#if duckIsVisible}
                    <img
                        class="duck-img"
                        src="wealth.jpg"
                        alt="class of graduates!"
                        in:fly={{ y: 200, duration: 2000 }}
                        out:fade
                    />
                {/if}
                <br />
            </div>
        {/snippet}

        {#snippet scrolly()}
            <ObservedArticleText callback={removeDuckCallback} {options}>
          
            </ObservedArticleText>

            <ObservedArticleText callback={showDuckCallback} {options}>
                 <code>duckIsVisible</code> to
                <code>true</code>.
                <br /><br />
                <code>duckIsVisible</code> 
                <code>duckIsVisible==true</code>, 
                <br /><br />
                
                <code>{"in:fly={{ y: 200, duration: 2000 }}"}</code>
            
            </ObservedArticleText>

            
        {/snippet}
    </Scroller>
</div>