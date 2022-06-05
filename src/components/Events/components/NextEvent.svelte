<script lang="ts">
    import Icon from "../../../../public/favicon.ico";
    const event = {
        city: "Coimbatore",
        icon: Icon,
        date: "15-12-2022",
        turf: "Dummy Turfs",
        link: "https://link.to/turf",
    };
</script>

<div class="next-event">
    <span class="top-decor">Next Event</span>
    <div class="event">
        <span class="city">{event.city}</span>
        <div class="details">
            <img src={event.icon} alt="event icon" />
            <div class="details-content">
                <span class="date">{event.date}</span>
                <span class="turf">{event.turf}</span>
            </div>
        </div>
        <a href={event.link}>View more</a>
    </div>
</div>

<style>
    .next-event {
        display: grid;
        grid-template-rows: auto 1fr;
    }

    .top-decor {
        border-bottom: 0.25em solid black;
    }
    .event {
        display: grid;
        grid-template-rows: auto 1fr auto;
        gap: 1em;
    }
    .city {
        font-size: 2em;
        font-weight: 600;
    }
    .details {
        display: grid;
        grid-template-columns: 1em 1fr;
        gap: 1em;
        align-items: center;
    }
    .details>img {
        width: 1em;
        height: 1em;
    }
    .details-content {
        display: grid;
        grid-template-rows: 1fr 1fr;
    }
</style>
