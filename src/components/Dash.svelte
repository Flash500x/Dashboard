<script>
    import Card from './Card.svelte';
    import Relay from './Relay.svelte';
    import { Waves } from 'lucide-svelte';
</script>
<div class='container'>
    <div class="header">
<h1>Dashboard</h1>
    <p>Realtime monitoring and intelligence</p>
    </div>
    <div class="card-container">
        <div class="first-row">
            <div><Card value='Soil Moisture' /></div>
            <div><Card value='Temperature' /></div>
            <div><Card value='Pressure' /></div>
        </div>
        <div class="second-row">
            <div><Card value='Light-Intensity'/></div>
            <div><Card value='Humidity'/></div>
            <div><Card value='Water Level'/></div>
        </div>
        <div class="first-row last-row">
            <div><Relay relay='Relay 1'/></div>
            <div><Relay relay='Relay 2'/></div>
        </div>
    </div>
</div>
<style>
    .container{
        width:80%;
        height:100vh;
        background-color: var(--body-color);
       
    }
    .header{
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        margin-left:5rem;
        margin-top:3rem;
    }
    h1,p{
        padding:0;
        margin:0;
    }
    p{
        color:var(--accent-text);
    }
    .card-container{
        height:50px;
        width:50px;
        margin-left:5rem;
        margin-top:2rem;
        display:flex;
        flex-direction: column;
        gap:3rem;  
    }
    .first-row ,.second-row{
        display:flex;
        flex-direction: row;
        gap:3rem;
    }
    .last-row{
        margin-left:6rem;
    }
</style>