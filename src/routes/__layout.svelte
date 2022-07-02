<script>
    import "$lib/css/global.css"
    import Header from "../lib/components/header.svelte";
    import Footer from "../lib/components/Footer.svelte";

    
</script>

<svelte:head>
    <link rel="stylesheet" href="https://use.typekit.net/kef0yis.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.1/css/all.min.css">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.1/css/all.min.css"></script>
</svelte:head>

<main>
    <Header/>
    <slot/>
    <Footer/>
</main>




