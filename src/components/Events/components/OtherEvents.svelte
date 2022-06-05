<script lang="ts">
    import { Svroller } from "svrollbar";
    import Icon from "../../../../public/favicon.ico";
    const events = {
        upcomming: [
            {
                icon: Icon,
                date: "25-12-2003",
                turf: "KCT Main turf Back side",
                link: "https://link.to/truf/event/",
            },
            {
                icon: Icon,
                date: "25-12-2003",
                turf: "KCT Main turf Back side",
                link: "https://link.to/truf/event/",
            },
            {
                icon: Icon,
                date: "25-12-2003",
                turf: "KCT Main turf Back side",
                link: "https://link.to/truf/event/",
            },
            {
                icon: Icon,
                date: "25-12-2003",
                turf: "KCT Main turf Back side",
                link: "https://link.to/truf/event/",
            },
        ],
        previous: [
            {
                icon: Icon,
                date: "25-12-2003",
                turf: "KCT Main turf Back side",
                link: "https://link.to/truf/event/",
            },
            {
                icon: Icon,
                date: "25-12-2003",
                turf: "KCT Main turf Back side",
                link: "https://link.to/truf/event/",
            },
            {
                icon: Icon,
                date: "25-12-2003",
                turf: "KCT Main turf Back side",
                link: "https://link.to/truf/event/",
            },
        ],
    };
</script>

<Svroller width="auto" height="75%">
    <div class="container">
        <div class="upcomming">
            {#each events.upcomming as event}
                <img src={event.icon} alt="icon" />
                <div class="event">
                    <span>{event.date}</span>
                    <span class="event-detail">
                        {event.turf}
                        <a href={event.link}>View More</a>
                    </span>
                </div>
            {/each}
        </div>
        <div class="previous">
            {#each events.upcomming as event}
                <img src={event.icon} alt="icon" />
                <div class="event">
                    <span>{event.date}</span>
                    <span class="event-detail">
                        {event.turf}
                        <a href={event.link}>View More</a>
                    </span>
                </div>
            {/each}
        </div>
    </div>
</Svroller>

<style>
    .container {
        height: 75%;
        /* overflow-y: scroll; */
        display: grid;
        grid-template-rows: 1fr 1fr;
        gap: 3em;
        padding: 2em;
    }

    .event {
        display: grid;
        grid-template-rows: 1fr 1fr;
    }

    .container > div {
        display: grid;
        grid-template-columns: 1em 1fr;
        align-items: center;
        gap: 1em;
        position: relative;
    }

    .event-detail {
        display: grid;
        grid-template-columns: 1fr auto;
        gap: 2em;
    }

    .container > div:before {
        position: absolute;
        inset: -2em 0 auto 0;
        border-bottom: 0.25em solid black;
    }

    .previous:before {
        content: "Previous";
    }

    .upcomming:before {
        content: "Upcomming";
    }
</style>
