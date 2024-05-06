<script>
    import Button from "@components/Button/Button.svelte";
</script>
<section class='section'>
    <div class='container'>
        <div class='info'>
            <h1>Join the CometChat partner universe </h1>
            <span>
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
                <input type="email" name="email" id="email" placeholder="Type your email...">
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
        padding: 8rem 4rem;

        background-image: url('../../assets/icons/stars.svg'),
        url('../../assets/icons/Gradient.svg'), 
            url('../../assets/icons/comet-mixed-orange.svg'), 
            url('../../assets/icons/comet-purple-half.svg'),
            url('../../assets/icons/comet-pink-half.svg'),
            url('../../assets/icons/comet-purple-small.svg');
        background-position: center, bottom, left, 0% 50%, 105% 85%, 50% 85%;
        background-repeat: no-repeat, no-repeat, no-repeat, no-repeat;
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
        max-width: 90rem;
        height: 4rem;
        border-radius: 14px;
        background: #FAFAFF05;
        border: 1px solid #FAFAFF1A;
        color: white;
    }

    @media screen and (max-width: 850px) {
        .container {
            flex-wrap: wrap;
        }
    }

</style>