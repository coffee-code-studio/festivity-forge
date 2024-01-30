<script>
    import '../app.css'
    import Navbar from '$lib/components/Navbar.svelte'
    import Footer from '$lib/components/Footer.svelte'
</script>

<style>
    :global(body) {
        background-color: #fff1f2;
    }
</style>

<Navbar />
<slot />
<Footer />