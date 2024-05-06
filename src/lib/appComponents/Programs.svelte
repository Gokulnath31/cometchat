<script>
        import ArrowsIcon from '@icons/arrows.svg';
        import TimeIcon from '@icons/time.svg';
        import SunIcon from '@icons/sun.svg';

        const programs =  [
            {
                icon: TimeIcon,
                title: 'Affiliate partner program',
                description: 'Bring value to your customers with a world-class in-app messaging tool that increases user-to-user engagement and retention. Get incentivized for referring CometChat to any of your customers.',
            },
            {
                icon: ArrowsIcon,
                title: 'Technology partner program',
                description: 'Development teams can use our plug and play solution to build top class chat solutions for their clients using our SDKs and APIs. It’s simple, safe and secure!',
            },
            {
                icon: SunIcon,
                title: 'Start up growth program',
                description: 'We help incubators, accelerators, co-working space that foster an ecosystem of start-ups. This program also enables VCs to accelerate the growth of their portfolio companies.',
            }
        ];
</script>
<section class='section'>
    <div class="container">
        <div class='section__header'>
            <span>Our programs</span>
            <h1>
                Types of partnerships programs
            </h1>
        </div>
        <div class='section__content'>
            <div class="program">
                {#each programs as program}
                    <div class='program__item'>
                        <span class='program__icon'>
                            <img class='program__icon-img' src={program.icon} alt='icon'/>
                        </span>
                        <h3 class='program__title'>{program.title}</h3>
                        <p class='program__description'>{program.description}</p>
                    </div>
                {/each}
            </div>
        </div>
    </div>
</section>

<style lang="scss">
    .container {
        width: 100%;
        max-width: 1200px;
        margin: 0 auto;
    }
    .section {
        background-color: white;
        color: black;
        padding: 8rem 4rem;
        

        &__header {
            font-size: 2.5rem;
            max-width: 100%;
            width: 600px;
            span {
                font-size: 2rem;
                color: #6852D6;
            }
            h1 {
                margin-top: 0;
                line-height: 1.2;
                color: black;
            }
        }
    }

    .program {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 2rem;
        justify-content: space-between;

        &__item {
            max-width: 30rem;
        }

        &__icon {
            width: 1rem;
            height: 1rem;

            &-img {
                max-width: 100%;
                max-height: 100%;
                object-fit: contain;
            }
        }

        &__title {
            font-size: 1.4rem;
            margin-top: 5px; 
        }

        &__description {
            font-size: 1.6rem;
        }
    }

    @media screen and (max-width: 780px) {
        .program {
            grid-template-columns: repeat(2, 1fr);
        }
    }


    @media screen and (max-width: 530px) {
        .program {
            grid-template-columns: 1fr;

            &__item {
                max-width: 100%;
            }
        }
    }
</style>