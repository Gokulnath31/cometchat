<script>
    import Button from "@components/Button/Button.svelte";
    import Logo from '@icons/logo.svg'
</script>

<nav>
    <ul class='nav-items'>
        <li class="logo"><img src={Logo} alt='comet-chat'/></li>
        <li class='section'><a href="#footer">Platform</a></li>
        <li class='section'><a href="#footer">Solutions</a></li>
        <li class='section'><a href="#footer">Developers</a></li>
        <li class='section'><a href="#footer">Resources</a></li>
        <li class='section'><a href="#reachout">Pricing</a></li>
        <li class='login'>Log in</li>
        <li class='section'><Button text='Schedule a demo'/></li>
    </ul>
</nav>

<style lang="scss">
    a {
        text-decoration:none; 
        color: white;
    }
    .nav-items {
        margin: 3rem;

        li:hover {
            cursor: pointer;
        }
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