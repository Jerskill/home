<script lang="ts">
    import NextEvent from "./components/NextEvent.svelte";
    import OtherEvents from "./components/OtherEvents.svelte";
</script>

<div class="events">
    <NextEvent />
    <OtherEvents />
</div>

<style>
    .events {
        display: grid;
        grid-template-rows: auto 1fr;
        gap: 2em;
        padding: 2em;
    }
</style>
