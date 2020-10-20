<script>
    import OneTrack from './OneTrack.svelte';

    let tracks = [
        {id: 1, imgPath: "./img/phones/ausine1.png", audioPath: "./mp3/1.mp3"},
        {id: 2, imgPath: "./img/phones/ausine2.png", audioPath: "./mp3/2.mp3"},
        {id: 3, imgPath: "./img/phones/ausine3.png", audioPath: "./mp3/3.mp3"},
        {id: 4, imgPath: "./img/phones/ausine4.png", audioPath: "./mp3/4.mp3"},
        {id: 5, imgPath: "./img/phones/ausine5.png", audioPath: "./mp3/5.mp3"},
        {id: 6, imgPath: "./img/phones/ausine6.png", audioPath: "./mp3/6.mp3"},
    ]

    let current = 0;

    function handleClick(id) {
        id === current ? current = 0 : current = id;
    }
</script>

<div class="tracks">
    {#each tracks as track}
        <OneTrack {...track} active={track.id === current} on:click={() => handleClick(track.id)}/>
    {/each}
</div>

<style>
    .tracks {
        display: grid;
        height: 100vh;
        top: 0;
        grid-template-columns: 1fr repeat(6, 4fr) 1fr; 
        grid-template-rows: repeat(12, 1fr);
        gap: 25px
    }

</style>