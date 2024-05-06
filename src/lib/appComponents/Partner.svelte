<script>
    import ArrowsIcon from '@icons/arrows.svg';
    import BookIcon from '@icons/book.svg';
    import CircleIcon from '@icons/circles.svg';
    import CropIcon from '@icons/crop.svg';
    import EarningIcon from '@icons/earning.svg';
    import QuestionMarkIcon from '@icons/question-mark.svg';
    import StatIcon from '@icons/stat.svg';
    import TimeIcon from '@icons/time.svg';
    import TVIcon from '@icons/tv.svg';

    const advantages = [
        {
            icon: CropIcon,
            title: 'Free credits',
            description: 'Empowering partners to scale.',
        },
        {
            icon: CircleIcon,
            title: 'Revenue share',
            description: 'Get monthly recurring revenues when you refer clients.',
        },
        {
            icon: TVIcon,
            title: 'Training and mentoring sessions',
            description: 'Enabling partners to deliver the best experience.',
        },
        {
            icon: ArrowsIcon,
            title: 'Special developer access',
            description: 'Get an all-access account to build unlimited PoCs for your clients.',
        },
        {
            icon: TimeIcon,
            title: 'Reduced time',
            description: 'Deliver your products much faster with our partners’ programs.',
        },
        {
            icon: StatIcon,
            title: 'Value addition to your users',
            description: 'We need a 2 line text here ',
        },
        {
            icon: BookIcon,
            title: 'Knowledge sessions',
            description: 'Access to product and market sessions.',
        },
        {
            icon: QuestionMarkIcon,
            title: 'On-demand support',
            description: 'Technical assistance for implementation.',
        },
        {
            icon: EarningIcon,
            title: 'Significant passive income',
            description: 'We need a 2 line text here ',
        },
    ]
</script>
<section class='section'>
    <div class="container">
        <div class='section__header'>
            <span>Be a partner</span>
            <h1>
                CometChat partner advantages
            </h1>
        </div>
        <div class='section__content'>
            <div class="advantage">
                {#each advantages as advantage}
                    <div class='advantage__item'>
                        <span class='advantage__icon'>
                            <img class='advantage__icon-img' src={advantage.icon} alt='icon'/>
                        </span>
                        <h3 class='advantage__title'>{advantage.title}</h3>
                        <p class='advantage__description'>{advantage.description}</p>
                    </div>
                {/each}
            </div>
        </div>
    </div>
    
</section>

<style lang="scss">
    .container {
        max-width: 100%;
        width: 1200px;
        margin: 0 auto;
    }
    .section {
        max-width: 100%;
        padding: 0 4rem;
        margin: 8rem auto;
        background-color: rgba(10, 9, 20, 1);

        &__header {
            font-size: 2.5rem;
            max-width: 100%;
            width: 600px;
            span {
                font-size: 2rem;
                color: #FF7F3E;
            }
            h1 {
                margin-top: 0;
                line-height: 1.2;
            }
        }
    }

    .advantage {
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
            color: #FAFAFF;
        }
        
    }

    @media screen and (max-width: 850px) {
        .advantage {
            grid-template-columns: repeat(2, 1fr);
        }
    }

    @media screen and (max-width: 470px) {
        .advantage {
            grid-template-columns: repeat(1, 1fr);
        }
    }
</style>
