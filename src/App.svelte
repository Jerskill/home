<script lang="ts">
  import "./styles/reset.css";
  import NavBar from "./components/NavBar/NavBar.svelte";
  import Header from "./components/Header/Header.svelte";
</script>

<div>
  <h1>JerSkill</h1>
  <NavBar />
  <Header />
</div>

<style>
  div {
    display: grid;
    grid-template-rows: auto auto 1fr;
    position: absolute;
    inset: 0;
    align-items: center;
  }
</style>
