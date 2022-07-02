<script>
    let year = new Date().getFullYear();
</script>

<section id="contact">
    <div class="inner">
        <div class="contact">
            <div class="title">contact</div>
            <div class="address">Jln. Hos Cokroaminoto, <br> Luwuk Banggai, Sulawesi Tengah, Indonesia</div>
            <div class="email">contact@chandrakobstanfilms.com</div>
            <div class="phone">+62 812 4221 6863</div>
            <div class="web">chandrakobstanfilms.com</div>
        </div>
        <div class="inquiry">
            <div class="title">inquiry</div>
            <input type="text" placeholder="Name*">
            <input type="email" placeholder="Email Address*">
            <textarea placeholder="Message"></textarea>
            <button>get in touch</button>
        </div>
    </div>
    <div class="foot">
        <ul class="social-links">
            <li>
                <a href="/"><i class="fa-brands fa-facebook-f"></i></a>
            </li>
            <li>
                <a href="/"><i class="fa-brands fa-instagram"></i></a>
            </li>
             <li>
                <a href="/"><i class="fa-brands fa-pinterest"></i></a>
            </li>
        </ul>
        <ul class="links">
            <li>
                <a href="/">About</a>
            </li>
            <li>
                <a href="/">Privacy Policy</a>
            </li>
            <li>
                <a href="/">FAQ</a>
            </li>
        </ul>
        <div class="copyright">
            Copyright {year} | chandrakobstanfilms.com - All rights reserved. <br> self-developed by diditamin.m
        </div>
    </div>
</section>


<style>
    section {
        min-height: 65vh;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        gap: 1rem;
        padding-bottom: 1rem;
    }
    
    .inner {
        padding: 1rem 15rem;
        margin-top: 2rem;

        display: flex;
        justify-content: flex-start;
        gap: 3rem;

        font-size: 20px;
        width: 100%;
    }

    .title {
        text-align: left;
        font-size: 29px;
        text-transform: uppercase;
        font-weight: 400;
    }

    .contact {
        display: flex;
        flex-direction: column;
        gap: 1rem;
    }

    .inquiry {
        display: flex;
        flex-direction: column;
        gap: 1rem;
        width: 60%;
    }


    .inquiry input {
        background-color: transparent;
        border: none;
        padding: 0.5rem;
        font-size: 20px;
        font-weight: 400;
        font-family: var(--adobe-font);

        outline: none;
        border-bottom: 1px solid #757575;
    }

    .inquiry textarea {
        background-color: transparent;
        border: none;
        padding: 0.5rem;
        font-size: 20px;
        font-weight: 400;
        font-family: var(--adobe-font);

        resize: none;
        outline: none;
        border-bottom: 1px solid #757575;
    }
    button {
        width: 30%;
        text-transform: uppercase;
        padding: 0.5rem;
        font-size: 15px;
        font-weight: 400;
        font-family: var(--adobe-font);
        background-color: transparent;
        border: 1px solid #757575;
        cursor: pointer;

    }

    ul {
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 2rem;
        text-transform: uppercase;
    }

    .foot {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 2rem;
        margin-top: 3rem;
        text-align: center;
    }
    
</style>