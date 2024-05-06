<script>
    import { onMount, onDestroy } from 'svelte';
    import { slide } from 'svelte/transition';
    import PlusIcon from '@icons/plus.svg';
    
    let body = null;
    let collapseContent = true;
    let makeCollapsible = false;

    let sizeObserver = new ResizeObserver(entries => {
        for (const entry of entries) {
            const { width } = entry.contentRect;
            if (width < 940) {
                makeCollapsible = true;
            } else {
                makeCollapsible = false;
            }
        }
    });
    
    onMount(() => {
       body = document.body;
        sizeObserver.observe(body);
    });

    onDestroy(() => {
        body && sizeObserver.unobserve(body);
    });

</script>

<section role="button" tabindex="0" class="collapsible-section" class:collapsible-section--expanded={!collapseContent}  on:click={() => collapseContent = !collapseContent}>
    <div class="collapsible-section__head">
        <span class="collapsible-section__title">
            <slot name="header"></slot>
        </span>
        {#if makeCollapsible}
            <span class="btn">
                <img class="chevron" class:chevron--down={collapseContent} src={PlusIcon} alt='expand|collapse'/>
            </span>    
        {/if}
    </div>
    {#if !collapseContent && makeCollapsible == true || makeCollapsible == false}
        <div class="collapsible-section__content" 
            transition:slide|local>
            <slot name="content">No content present to show</slot>
        </div>
    {/if}
</section>

<style lang="scss">
    .collapsible-section {
        width:100%;
        background: rgba(20, 19, 29, 0.02);
        padding: 1rem 1rem;
        margin-top: 1rem;

        &:hover {
            cursor: pointer;
        }

        &--expanded &__title{
            font-weight: 500;
        }

        &__head {
            width: 100%;
            margin-bottom: 5px;
            display: flex;
            flex-direction: row;
            align-items: center;
            flex-wrap: wrap;
            line-height: 1.2;
        }

        &__title {
            max-width: calc(100% - 20px);
            margin-right: auto;
            font-size: 1.8rem;
            font-weight: normal;
            color:black;
        }
    }

    .btn {
        background-color: transparent;

        &:hover {
            cursor: pointer;
        }
    }

    .chevron {
        width: 1.5rem;
        transition: all .4s;
        border: 0;

        &--down {
            transform: rotate(180deg) ;
        }
    }

</style>