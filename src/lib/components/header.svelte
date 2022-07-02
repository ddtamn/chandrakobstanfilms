<script>
    let scrollY;
</script>

<svelte:window bind:scrollY={scrollY}/>

<header class="{scrollY > 0 ? 'sticky' : ''}">
    <div class="container">
        <div class="logo">Chandrakobstan <span>films</span></div>
        <nav>
            <ul>
                <li class="active">
                    <a href="/">Home</a>
                </li>
                <li>
                    <a href="/about">About</a>
                </li>
                <li>
                    <a href="/">Journal</a>
                </li>
                <li>
                    <a href="#contact">Contact</a>
                </li>
            </ul>
        </nav>
        <div class="social-links">
            <ul>
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
        </div>
    </div>
</header>

<style>
    header {
        position: fixed;
        top: 0;
        left: 0;
        height: 45px;
        width: 100%;
        background-color: transparent;
        color: var(--fn-white-color);
        z-index: 999;
    }

    header.sticky .container {
        background-color: var(--fn-color);
        transition: all 0.4s ease-in-out;
    }

    header.sticky .logo {
        font-size: 20px;
         transition: all 0.4s ease-in-out;
    }
    .container {
        display: flex;
        justify-content: space-between;
        padding: 1rem 8rem;
        align-items: center;
    }

    .logo {
        font-size: 28px;
         transition: all 0.4s ease-in-out;
    }

    nav {
        margin-left: -8rem;
    }

    ul {
        display: flex;
        align-items: center;
        gap: 2rem;
        font-size: 13px;
        text-transform: uppercase;
    }

    li {
        line-height: 1.8;
        transition: all 0.1s ease-in-out;
        background-image: linear-gradient(currentColor,currentColor);
        background-repeat: repeat-x;
        background-size: 1px 1px;
        background-position: 0 110%;
    }

    li.active, li:hover {
        background-position: 0 100%;
    }

    


</style>