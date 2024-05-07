<script>
	import Button from "@components/Button/Button.svelte";

</script>
<section class='section' id='reachout'>
    <div class="container">
        <h1>Get started for free</h1>
        <p>
            Build and test for as long as you need. 
        </p>
        <p>
            Pick a plan when you’re ready.
        </p>
        <div class=section__actions>
            <Button text='Start free trial' --btn-color='rgba(250, 250, 255, 0.02)'/>
            <Button text='Schedule a demo'/>
        </div>
    </div>
    
</section>

<style lang="scss">
    .container {
        width: 100%;
        max-width: 600px;
        margin: 0 auto;

        h1 {
            font-size: 4.8rem;
            margin-bottom: 5px;
        }

        p {
            font-weight: 300;
            color: rgba(250, 250, 255, 1);

        }
    }
    .section {
        margin: 0 auto;
        padding: 10rem 4rem;
        text-align: center;

        background-image: url('../../assets/images/bg-stars.svg'), 
            url('../../assets/images/bg-blue-galaxy.svg'), 
            url('../../assets/images/bg-comet-purple.svg'), 
            url('../../assets/images/bg-comet-orange.svg');
        background-position: center, center bottom, left bottom, right top;
        background-repeat: no-repeat, no-repeat, no-repeat;
        background-blend-mode: multiply;

        &__actions {
            margin-top: 2rem;
        }
    }

    @media screen and (max-width: 870px) {
        .section {
            background-image: url('../../assets/images/bg-stars.svg'), 
                url('../../assets/images/bg-blue-galaxy.svg'), 
                url('../../assets/images/bg-comet-pink-right.svg'), 
                url('../../assets/images/bg-comet-orange-half.svg');
            background-position: center, center bottom, left top, right bottom;
        }
       
    }

</style>