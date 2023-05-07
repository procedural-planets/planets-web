<script lang="ts">
    import type { Image } from './Image';

    export let entry_title: string;
    export let entry_text: string;
    export let entry_date: string;
    export let entry_image: Image | null;
</script>

<div class="journal-entry">
    <h2>{entry_title}</h2>
    <p class="date">{entry_date}</p>
    {#if entry_image != null}
    <div class="image">
        <img src={entry_image.src} alt={entry_image.desc}>
        <p>{entry_image.text}</p>
    </div>
    {/if}
    <p>{entry_text}</p>
</div>

<style lang="scss">
    .journal-entry {
        background-color: rgb(9, 41, 39);
        width: 100%;
        border-radius: 15px;
        box-shadow: 0 4px 6px 0 #00000033;
        padding: 1em 2em 2em 2em;
        margin-bottom: 4em;
    }

    .date {
        color: rgb(118, 153, 151);
        font-weight: bold;
        padding-top: 0;
    }

    img {
        width: 100%;
        border-radius: 10px;
        margin-top: 1em;
    }

    .image p {
        padding-top: 0;
        font-size: 90%;
        font-style: italic;
        position: relative;
        left: 1vw;
    }

    p {
        padding-top: 1em;
        white-space: pre-line;
    }
</style>