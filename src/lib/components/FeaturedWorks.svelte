<script>

    let source = [
        {link : 'https://source.unsplash.com/random/900x600/?wedding'},
        {link : 'https://source.unsplash.com/random/900x600/?wedding-moment'},
        {link : 'https://source.unsplash.com/random/900x600/?wedding-party'},
        {link : 'https://source.unsplash.com/random/900x600/?wedding-sumba'},
        {link : 'https://source.unsplash.com/random/900x600/?wedding-gallery'},
        {link : 'https://source.unsplash.com/random/900x600/?couple-session'},
        {link : 'https://source.unsplash.com/random/900x600/?prewedding'},
        {link : 'https://source.unsplash.com/random/900x600/?prewedding-moment'},
        {link : 'https://source.unsplash.com/random/900x600/?prewedding-gallery'},
    ]
</script>

<section>
        <div class="inner">
             <h1 class="title">featured works</h1>
       <div class="works">
            {#each source as source}
                
            <div class="work">
                <a class="image" href="/"><img src="{source.link}" alt=""></a>
                <div class="description">Moyo & Wiwid | Prewedding</div>
            </div>
            {/each}
           
        </div>
       </div>
    </section>


    <style>
        section {
            min-height: 65vh;
            display: flex;
            align-items: center;
        }

        .inner {
            padding: 3rem 1rem;
            padding-top: 7rem;
        }

        .title {
            text-align: center;
            font-size: 29px;
            text-transform: uppercase;
            font-weight: 400;

        }

        .works {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 1rem;
            margin-top: 2rem;
            flex-wrap: wrap;
            width: 100%;

        }

        .work {
            width: calc(100% / 4);
            margin-bottom: 1rem;
            overflow: hidden;
            
        }


        .work .image img {
            width:100%;
            object-fit: cover;
        }


    </style>