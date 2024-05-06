<script>
    export let text;

</script>
<button class='btn'>{text}</button>

<style lang="scss">
    button {
        padding: 12px 16px 12px 16px;
        border-radius: 12px;
        color: white;
        background-color: var(--btn-color, rgba(104, 82, 214, 1));

        &:hover {
            cursor: pointer;
        }
    }
   
</style>