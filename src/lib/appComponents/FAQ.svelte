<script>
    import Collapsible from "@components/Collapsible/Collapsible.svelte";
    const faqs = [
        {
            question: 'This is a frequently asked question?',
            answer: 'Lorem ipsum dolor sit amet consectetur. Tellus eget consequat tortor odio maecenas cursus leo dui. Pulvinar quam sit quam feugiat laoreet morbi tellus dui massa.',
        },
        {
            question: 'This is a frequently asked question?',
            answer: 'Lorem ipsum dolor sit amet consectetur. Tellus eget consequat tortor odio maecenas cursus leo dui. Pulvinar quam sit quam feugiat laoreet morbi tellus dui massa.',
        },
        {
            question: 'This is a very long frequently asked question about our services with more than one line?',
            answer: 'Lorem ipsum dolor sit amet consectetur. Tellus eget consequat tortor odio maecenas cursus leo dui. Pulvinar quam sit quam feugiat laoreet morbi tellus dui massa.',
        },
        {
            question: 'This is a frequently asked question?',
            answer: 'Lorem ipsum dolor sit amet consectetur. Tellus eget consequat tortor odio maecenas cursus leo dui. Pulvinar quam sit quam feugiat laoreet morbi tellus dui massa.',
        },
        {
            question: 'This is a question?',
            answer: 'Lorem ipsum dolor sit amet consectetur. Tellus eget consequat tortor odio maecenas cursus leo dui. Pulvinar quam sit quam feugiat laoreet morbi tellus dui massa.',
        },
        {
            question: 'This is a question?',
            answer: 'Lorem ipsum dolor sit amet consectetur. Tellus eget consequat tortor odio maecenas cursus leo dui. Pulvinar quam sit quam feugiat laoreet morbi tellus dui massa.',
        }

    ]
</script>
<section class='section'>
    <div class="container">
        <div class='section__header'>
            <span class='heading-tertiary'>FAQ</span>
            <h1 class=heading-primary>
                We want to help you with all your doubts 
            </h1>
        </div>
        <div class='section__content'>
            <div class="faq">
                {#each faqs as faq}
                    <div class='faq__item'>
                        <Collapsible>
                            <span slot="header">{faq.question}</span>
                            <span slot="content">{faq.answer}</span>
                            {faq.answer}
                        </Collapsible>
                    </div>
                {/each}
            </div>
        </div>
    </div>
   
</section>

<style lang="scss">
    .container {
        width: 100%;
        max-width: 600px;
        margin: 0 auto;
    }
    .section {
        background-color: white;
        color: black;
        padding: 12rem 4rem;

        &__header {
            font-size: 2.5rem;
            max-width: 100%;
            width: 600px;
            span {
                display: inline-block;
                width: 100%;
                text-align: center;
                color: #FF7F3E;
            }
            h1 {
                margin-top: 0;
                line-height: 1.2;
                color: black;
            }
        }
    }

    @media screen and (max-width: 420px) {
        .section {
            padding-left: 1.5rem;
            padding-right: 1.5rem;
        }
    }
</style>