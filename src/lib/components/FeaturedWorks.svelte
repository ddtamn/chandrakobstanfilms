<script>
    let image1 = "src/lib/images/img001.jpg"
    let image2 = "src/lib/images/img002.jpg"
    let image3  = "src/lib/images/img003.jpg"
    let image4  = "src/lib/images/img004.jpg"
</script>

<section>
        <div class="inner">
             <h1 class="title">featured works</h1>
       <div class="works">
            <div class="work">
                <a class="image" href="/"><img src="{image4}" alt=""></a>
                <div class="description">Moyo & Wiwid | Prewedding</div>
            </div>
            <div class="work">
                <a class="image" href="/"><img src="{image4}" alt=""></a>
                <div class="description">Moyo & Wiwid | Prewedding</div>
            </div>
            <div class="work">
                <a class="image" href="/"><img src="{image4}" alt=""></a>
                <div class="description">Moyo & Wiwid | Prewedding</div>
            </div>
            <div class="work">
                <a class="image" href="/"><img src="{image4}" alt=""></a>
                <div class="description">Moyo & Wiwid | Prewedding</div>
            </div>
            <div class="work">
                <a class="image" href="/"><img src="{image4}" alt=""></a>
                <div class="description">Moyo & Wiwid | Prewedding</div>
            </div>
            <div class="work">
                <a class="image" href="/"><img src="{image4}" alt=""></a>
                <div class="description">Moyo & Wiwid | Prewedding</div>
            </div>
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