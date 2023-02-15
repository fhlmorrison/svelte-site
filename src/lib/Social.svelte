<script>
    export let href;
    export let text;
</script>

<div class="social">
    <div class="icon">
        <slot />
    </div>
    <a {href} target="_blank" rel="noreferrer"> {text} </a>
</div>

<style>
    .social {
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .icon {
        display: inline-block;
        height: 2em;
        width: 2em;
    }
</style>
