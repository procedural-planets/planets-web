<script>
    /**
     * @type {string}
     */
     export let entry_title;
     /**
     * @type {string}
     */
    export let entry_text;
    /**
     * @type {string}
     */
     export let entry_date;
</script>

<div class="journal-entry">
    <h2>{entry_title}</h2>
    <p class="date">{entry_date}</p>
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

    p {
        padding-top: 1em;
        white-space: pre-line;
    }
</style>