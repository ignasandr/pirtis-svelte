<script>
    // import {Howl, Howler} from 'howler';
    export let id, imgPath, active;

    // var track = new Howl({
    //     src: [audioPath]
    // });

    // function playTrack() {
    //     active ? track.stop() : track.play();
    // }

</script>

<div id="track{id}" class="{active ? "OneTrack active" : "OneTrack"}" on:click>
    <img src={imgPath} alt="phones"> 
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
