<script lang="ts">
    import Events from "../Events/Events.svelte";
    import News from "./components/News.svelte";
    import bgVideo from "../../assets/bg.mp4";
</script>

<header>
    <Events />
    <News />
    <!--<video src={bgVideo} autoplay>
        <track kind="captions" />
    </video>-->
</header>

<style>
    header {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 2em;
        justify-items: center;
        align-items: center;
    }

    video {
        position: absolute;
        inset: 0;
        z-index: -999;
        width: 100vw;
        height: 100vh;
        opacity: 0.75;
    }
</style>
