<script>
    import Button from "@components/Button/Button.svelte";
    import Logo from '@icons/logo.svg'
</script>

<nav>
    <ul class='nav-items'>
        <li class="logo"><img src={Logo} alt='comet-chat'/></li>
        <li class='section'>Platform</li>
        <li class='section'>Solutions</li>
        <li class='section'>Developers</li>
        <li class='section'>Resources</li>
        <li class='section'>Pricing</li>
        <li class='login'>Log in</li>
        <li class='section'><Button text='Schedule a demo'/></li>
    </ul>
</nav>

<style lang="scss">
    .nav-items {
        margin: 3rem;
    }
    ul { 
        list-style: none; 
        display: flex;
        align-items: center;
        gap: 2rem;
    }
    .logo {
        margin-right: auto;
    }
    .login {
        margin-left: auto;
    }

    @media screen and (max-width: 950px) {
        .logo {
            width: 9rem;
            height: 1.6rem; 
            img {
                max-width: 100%;
                max-height: 100%;
            }
        }
        .section {
            display: none;
        }
    }
</style>