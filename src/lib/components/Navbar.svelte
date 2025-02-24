<script>
  import { goto } from "$app/navigation";

  const navLinks = [
    { name: "Home", path: "/" },
    { name: "Speakers", path: "/speakers" },
    { name: "Schedule", path: "/schedule" },
    { name: "Sponsors", path: "/sponsors" },
    { name: "About", path: "/about" },
    { name: "Contact", path: "/contact" }
  ];
</script>

<nav class="navbar">
  <button class="logo" on:click={() => goto("/")}>TechConf 2025</button>
  <ul>
    {#each navLinks as link}
      <li><a href={link.path}>{link.name}</a></li>
    {/each}
  </ul>
</nav>

<style>
  .navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: #222;
    color: white;
    padding: 1rem 2rem;
  }
  .logo {
    font-size: 1.5rem;
    font-weight: bold;
    cursor: pointer;
    background: none;
    border: none;
    color: white;
    font-family: inherit;
    padding: 0;
  }
  ul {
    list-style: none;
    display: flex;
    gap: 1.5rem;
  }
  li a {
    text-decoration: none;
    color: white;
    transition: 0.3s;
  }
  li a:hover {
    color: #ff6600;
  }
</style>
