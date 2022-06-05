<script lang="ts">
    import { Svroller } from "svrollbar";

    const news = [
        {
            title: "this is tile 1",
            description: "this is clean nice description for the news 1",
            link: "https://this.is.the.page.to/continue/?item=1",
        },
        {
            title: "this is tile 2",
            description: "this is clean nice description for the news 2",
            link: "https://this.is.the.page.to/continue/?item=2",
        },
        {
            title: "this is tile 3",
            description: "this is clean nice description for the news 3",
            link: "https://this.is.the.page.to/continue/?item=3",
        },
        {
            title: "this is tile 4",
            description: "this is clean nice description for the news 4",
            link: "https://this.is.the.page.to/continue/?item=4",
        },
        {
            title: "this is tile 5",
            description: "this is clean nice description for the news 5",
            link: "https://this.is.the.page.to/continue/?item=5",
        },
        {
            title: "this is tile 6",
            description: "this is clean nice description for the news 6",
            link: "https://this.is.the.page.to/continue/?item=6",
        },
    ];
</script>

<Svroller width="auto" height="50%">
    <div class="contents">
        {#each news as news}
            {@const { title, description, link } = news}
            <a class="container" href={link}>
                <h3>{title}</h3>
                <p class="description">{description}</p>
            </a>
        {/each}
    </div>
</Svroller>

<style>
    div {
        display: flex;
        flex-direction: column;
        gap: 2em;
        height: 50%;
        /* overflow-y: scroll; */
        padding: 2em;
    }

    a {
        text-decoration: none;
        color: inherit;
    }
</style>
