<div class="sponsors">
    <img src="./img/sponsors/mc.png" alt="magic carpets logo"/>
    <img src="./img/sponsors/lkt.png" alt="lietuvos kulturos taryba logo"/>
    <img src="./img/sponsors/bienale.png" alt="bienale logo"/>
    <img src="./img/sponsors/eu.png" alt="eu logo"/>
    <img src="./img/sponsors/k3022.jpg" alt="kaunas 3022 logo"/>
</div> 

<style>
    .sponsors {
        display: flex;
        justify-content: space-around;
        align-items: center;
        height: 80px;
        background-color: #e3e0da;
        padding: 5px 20px;
    }

    .sponsors img {
        height: 80%;
    }

    @media (max-width: 576px) { 
        .sponsors {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        padding: 5px 5px 5px 60px;
        }

        .sponsors img:last-child {
        grid-row-start: 2;
        }
    }
</style>