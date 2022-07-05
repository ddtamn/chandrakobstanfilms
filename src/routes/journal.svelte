<script>
    let activeCategory = 'all'
    let GOOGLE_DRIVE_EXPORT_LINK = 'http://drive.google.com/uc?export=view&id='
    let img1 = GOOGLE_DRIVE_EXPORT_LINK + '14Omn4Kmo6kBp0Bc2ZZ3g2ksFWNhWee3U'
</script>

<section>
    <div class="jumbotron" style="background-image: url({img1});">
        <div class="title">explore our works</div>
        <div class="overlay"></div>
    </div>
    <div class="journal" id="j">
        <div class="categories">
            <ul>
                <li on:click="{() => activeCategory = 'all'}" class="{activeCategory == 'all' ? 'active' : ''}">
                    <a href="/journal#j">All</a>
                </li>
                <li on:click="{() => activeCategory = 'wedding'}" class="{activeCategory == 'wedding' ? 'active' : ''}">
                    <a href="/journal?category=wedding#j">Wedding</a>
                </li>
                <li on:click="{() => activeCategory = 'prewedding'}" class="{activeCategory == 'prewedding' ? 'active' : ''}">
                    <a href="/journal?category=prewedding#j">Prewedding</a>
                </li>
                <li on:click="{() => activeCategory = 'other'}" class="{activeCategory == 'other' ? 'active' : ''}">
                    <a href="/journal?category=other#j">Other</a>
                </li>
            </ul>
        </div>
    </div>
</section>


<style>
    .jumbotron {
        min-height: 100vh;
        background-position: center center;
        background-repeat: no-repeat;
        background-size: cover;

        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        color: var(--fn-white-color);
        letter-spacing: 2px;
        font-size: 40px;
        font-weight: 100;
        text-transform: uppercase;

        position: relative;
    }

    .overlay {
        position: absolute;
        height: 100%;
        width: 100%;
        top: 0;
        left: 0;
        background-color: black;
        opacity: 0.4;
    }

    .title {
        position: absolute;
        z-index: 1;
    }

    .journal {
        min-height: 100vh;
        padding: 1rem;
        padding-top: 3rem;
    }

    .categories ul {
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        gap: 1rem;
        color: #7d7d7d;
        font-size: 20px;
    }

    .categories li.active {
        color: var(--fn-color);
    }
</style>