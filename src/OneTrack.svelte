<script context="module">
    let current;
</script>

<script>
    export let id, imgPath, audioPath, active;

    let audio;
    let paused = true;

    function stopOthers() {
        if (current && current !== audio) current.pause();
        current = audio;
    }

    function startPlaying() {
        if (paused) {
            audio.currentTime = 0;
            audio.play();
        }
        else {
            audio.pause();
        }
    }

</script>

<div id="track{id}" class="{active ? "OneTrack active" : "OneTrack"}" on:click>
    <img src={imgPath} alt="phones" on:click={startPlaying}> 
    <audio
        bind:this={audio}
        bind:paused
        on:play={stopOthers}
        src={audioPath}>
        <track kind="captions">
    </audio>
</div>

<style>
    img {
        position: absolute;
        left: 0;
        bottom: 0;
        max-width: 100%;
    }

    .OneTrack {
        /* height: 40%; */
        position: relative;
        opacity: 40%;
        transition: opacity 0.5s ease-in-out;
        /* background-color: blue; */
    }

    .OneTrack:hover {
        opacity: 100%;
        cursor: pointer;
    }

    .active {
        opacity: 100%;
    }
</style>
