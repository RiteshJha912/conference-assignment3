<script>
  import { onMount } from "svelte";
  import { goto } from "$app/navigation";
//   import HeroImage from "$lib/assets/hero.jpg"; // Replace with actual image path

  let speakers = [
    { name: "Alice Johnson", image: "/assets/speaker1.jpg" },
    { name: "Bob Williams", image: "/assets/speaker2.jpg" },
    { name: "Charlie Brown", image: "/assets/speaker3.jpg" }
  ];

  function register() {
    goto("/register");
  }
</script>

<!-- Hero Section -->
<section class="hero">
  <div class="content">
    <h1>Tech Conference 2025</h1>
    <p>Join industry leaders, developers, and innovators for an unforgettable experience!</p>
    <button on:click={register}>Register Now</button>
  </div>
</section>

<!-- Featured Speakers -->
<section class="speakers">
  <h2>Featured Speakers</h2>
  <div class="grid">
    {#each speakers as speaker}
      <div class="speaker">
        <img src={speaker.image} alt={speaker.name} />
        <h3>{speaker.name}</h3>
      </div>
    {/each}
  </div>
</section>

<style>
  .hero {
    background: url({HeroImage}) center/cover no-repeat;
    height: 60vh;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    text-align: center;
  }
  .hero .content {
    background: rgba(0, 0, 0, 0.6);
    padding: 2rem;
    border-radius: 8px;
  }
  .hero button {
    padding: 10px 20px;
    font-size: 1.2rem;
    cursor: pointer;
    border: none;
    background: #ff6600;
    color: white;
    border-radius: 5px;
  }
  .speakers {
    text-align: center;
    padding: 3rem 1rem;
  }
  .grid {
    display: flex;
    justify-content: center;
    gap: 2rem;
    flex-wrap: wrap;
  }
  .speaker {
    text-align: center;
  }
  .speaker img {
    width: 150px;
    height: 150px;
    border-radius: 50%;
  }
</style>
