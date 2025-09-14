<script>
  // default prop if nothing is passed
  export let relay = "Relay 1";

  import Switch from './Switch.svelte';
  
  let isOn = false; 
</script>

<div class="card">
  <div>
    <h1 class="header">{relay}</h1>
  </div>

  <div>
    <h1 class="value">Pump</h1>

    <div class="toggle-mode">
      <Switch bind:checked={isOn} />
      <p>{isOn ? "ON" : "OFF"}</p>
    </div>
  </div>

  <div class="divider"></div>
  <p class="time">Last updated 12:05:79</p>
</div>

<style>
  .card {
    width: 230px;
    border-radius: 5px;
    padding: 1rem;
    margin: 0;
    background-color: #23272F;
    color: #fff;
  }
  .divider {
    height: 1px;
    background: gray;
    margin: 0.5rem 0;
  }
  .header {
    margin-top: -5px;
    font-size: 20px;
  }
  .value {
    margin-top: -10px;
    font-size: 2.5rem;
  }
  .toggle-mode {
    display: flex;
    align-items: center;
    gap: 1rem;
  }
  .time {
    margin-bottom: -6px;
    margin-top: 1px;
    opacity: 50%;
    font-size: 0.7rem;
  }
</style>