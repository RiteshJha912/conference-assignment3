<script>
  import Navbar from "$lib/components/Navbar.svelte";
  import Footer from "$lib/components/Footer.svelte";
</script>

<Navbar />
<slot /> <!-- This is where the page content will load -->
<Footer />
