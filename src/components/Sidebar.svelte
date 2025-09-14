<script>
  export let user = {
    name: "User 1",
    role: "Online",
    avatar: "https://i.pravatar.cc/40" // you can replace with your own
  };

  let active = "dashboard";
import { Sprout } from 'lucide-svelte';

</script>
<style>
   
  .sidebar {
    width: 20%;
    height: 97vh;
    background-color: #23272F;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    padding: 1rem;
  }

  .header {
    font-size: 1.5rem;
    font-weight: bold;
    margin-bottom: 2rem;
    text-align: center;
    border-bottom:1px solid #333;
    padding-bottom:1rem;
    color:var(--accent-color);
  }

  .nav {
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }

  .nav button {
    all: unset;
    cursor: pointer;
    padding: 0.75rem 1rem;
    border-radius: 0.5rem;
    font-size: 1rem;
    color: #ddd;
    transition: background 0.2s;
  }

  .nav button:hover {
    background: #2a2d33;
  }

  .nav button.active {
    background: var(--accent-color);
    color: white;
  }

  .footer {
    border-top: 1px solid #333;
    padding-top: 1rem;
    display: flex;
    align-items: center;
    gap: 0.75rem;
  }

  .footer img {
    border-radius: 50%;
    width: 40px;
    height: 40px;
  }

  .footer .info {
    display: flex;
    flex-direction: column;
    font-size: 0.85rem;
  }

  .footer .info span {
    opacity: 0.8;
    font-size: 0.75rem;
  }
</style>

<div class="sidebar">
  <!-- Header -->
  <div>
   
    <div class="header"><Sprout /> AgroSense</div>

    <!-- Navigation -->
    <div class="nav">
      <button 
        class:active={active === "dashboard"} 
        on:click={() => active = "dashboard"}>
        Dashboard
      </button>
     
    </div>
  </div>

  <!-- Footer User Profile -->
  <div class="footer">
    <img src={user.avatar} alt="User avatar" />
    <div class="info">
      <strong>{user.name}</strong>
      <span>{user.role}</span>
    </div>
  </div>
</div>