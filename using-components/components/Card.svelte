<script>
    // VID 22
    // export let content;
</script>

<div class="card">
    <!-- VID 22 -->
    <!-- <slot>
        Default content
    </slot> -->

    <!-- VID 23 -->
    <div class="card-header">
        <slot name="header"></slot>
    </div>
    <div class="card-content">
        <slot name="content">Default content</slot>
    </div>
    {#if $$slots.footer}
    <hr />
    {/if}
    <div class="card-footer">
        <slot name="footer"></slot>
    </div>
</div>

<style>
    .card {
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
        transition: 0.3s;
        padding: 16px;
        margin-bottom: 20px;
        width: 200px;
    }

    .card:hover {
        box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
    }
</style>