<script>
    import Button from "@components/Button/Button.svelte";
    import Logos from '@icons/logos.svg'
</script>
<section class='section'>
    <div class='container'>
        <div class='info'>
            <h1 class=heading-primary>Join the CometChat partner universe </h1>
            <span class='heading-tertiary'>
                Create value for your clients, leveraging our world-class technology. Partner with us and grow your business!
            </span>
        </div>
        <div id='reachout-form' class='form'>
            <h2 class=form__header>Become a partner</h2>
            <label>
                Full name<br />
                <input type="text" name="fullname" id="fullname" placeholder="Type your name here...">
            </label>
            <label>
                Email address<br />
                <input class='fontAwesome' type="email" name="email" id="email" placeholder="Type your email...">
            </label>
            <label>
                Company's name<br />
                <input type="text" name="companyname" id="companyname" placeholder="Type you company’s name">
            </label>
            <br />
            <Button text='Submit application'/>
        </div>
    </div>
</section>
<div class='clients'>
    <img class='clients__logos' src={Logos} alt='clients' />
</div>


<style lang="scss">
    .container {
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 5rem;
        width: 100%;
        margin: 0 auto;
    }

    .section {
        margin: 0 auto;
        padding: 12rem 4rem;

        background-image: url('../../assets/images/bg-stars.svg'),
        url('../../assets/images/bg-Gradient.svg'), 
            url('../../assets/images/bg-comet-mixed-orange.svg'), 
            url('../../assets/images/bg-comet-purple-half.svg'),
            url('../../assets/images/bg-comet-pink-half.svg'),
            url('../../assets/images/bg-comet-purple-small.svg');
        background-position: center, bottom, left, 0% 50%, 105% 85%, 50% 85%;
        background-repeat: no-repeat, repeat-x, no-repeat, no-repeat,  no-repeat, no-repeat;
        background-blend-mode: multiply;
    }

    .info {
        align-self: baseline;
        margin-top: 2rem;
        width: 48rem;
        h1 {
            line-height: 1.2;
        }
        span {
            font-weight: 300;
        }
    }
    .form {
        &__header {
            margin-bottom: 10px;
        }
    }
    #reachout-form {
        display: flex;
        flex-direction: column;
        width: 52rem;
        padding: 3rem;
        border-radius: 24px;
        background: rgba(250, 250, 255, 0.08);
        backdrop-filter: blur(20px)
    }

    label {
        margin-top: 8px;
    }

    input {
        width: 100%;
        padding: 0.8rem 1rem 1rem;
        max-width: 90rem;
        height: 4rem;
        border-radius: 14px;
        background: #FAFAFF05;
        border: 1px solid #FAFAFF1A;
        color: white;
    }

    .clients {
        width: 100%;
        padding: 4rem 0;
        max-width: 100%;
        overflow: hidden;
        &__logos {
            object-fit: cover;
        }
    }

    @media screen and (max-width: 850px) {
        .container {
            flex-wrap: wrap;
        }

        .section {
            padding-block: 2rem;
            background-image: url('../../assets/images/bg-stars.svg'),
                url('../../assets/images/bg-Gradient.svg'), 
                url('../../assets/images/bg-comet-purple-half.svg'),
                url('../../assets/images/bg-comet-pink-half.svg');
            background-position: center, bottom, 0% 50%, 120% 120%;
            background-repeat: no-repeat, repeat-x, no-repeat, no-repeat;
            background-blend-mode: multiply;
        }
    }

    @media screen and (max-width: 420px) {
        .section {
            padding-left: 1.5rem;
            padding-right: 1.5rem;
        }
    }

</style>