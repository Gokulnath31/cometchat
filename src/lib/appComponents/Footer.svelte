<script>
        import CollapsibleList from '@components/CollapsibleList/CollapsibleList.svelte';
        import FacebookIcon from '@icons/facebook.svg';
        import InstagramIcon from '@icons/instagram.svg';
        import GithubIcon from '@icons/github.svg';
        import LinkedInIcon from '@icons/linkedin.svg';
        import TwitterIcon from '@icons/twitter.svg';
</script>
<section class='section'>
    <div class="container">
        <div class='items-list'>
            <div class='items' id='tech'>
                <CollapsibleList>
                    <span slot='header' class='items__title'>Platform</span>
                    <ul slot='content'>
                        <li>
                            <span class='items__grp-title'>Features</span>
                            <ul class='list__nested'>
                                <li>Chat & Messaging</li>
                                <li>Voice & Video Calls</li>
                                <li>Security & Compliance</li>
                                <li>Extensions</li>
                                <li>Features at a glance</li>
                                <li>Webhooks & Bots</li>
                                <li>Moderation</li>
                                <li>Analytics & Insights</li>
                            </ul>
                        </li>
                        <li>
                            <span class='items__grp-title'>Implementation</span>
                            <ul class='list__nested'>
                                <li>Widgets</li>
                                <li>UI Kits</li>
                                <li>SDKs & APIs</li>
                            </ul>
                        </li>
                        <li>
                            <span class='items__grp-title'>Technologies</span>
                            <ul class='list__nested'>
                                <li>React Chat SDK & API</li>
                                <li>Angular Chat SDK & API</li>
                                <li>Vue Chat SDK & API</li>
                                <li>IOS Swift Chat SDK & API</li>
                                <li>Android Kotlin Chat SDK & API</li>
                                <li>Android Java Chat SDK & API</li>
                                <li>React Native Chat SDK & API</li>
                                <li>Ionic/Capacitor Chat SDK & API</li>
                                <li>WordPress Chat SDK & API</li>
                                <li>Laravel/PHP Chat SDK & API</li>
                                <li>Flutter Chat SDK & API</li>
                                <li>Next.js Chat SDK & API</li>
                            </ul>
                        </li>
                    </ul>
                </CollapsibleList>
            </div>
            <div class="items" id='solutions'>
                <CollapsibleList>
                    <span slot='header' class='items__title'>Solutions</span>
                    <ul slot='content'>
                        <li>
                            <span class='items__grp-title'>By Use Cases</span>
                          <ul>
                            <li>Social Community</li>
                            <li>Marketplace</li>
                            <li>Healthcare</li>
                            <li>Education</li>
                            <li>Virtual Events</li>
                            <li>On-Demand Service</li>
                            <li>Dating Apps</li>
                            <li>Gaming</li>
                          </ul>
                        </li>
                        <li>
                            <span class='items__grp-title'>By Organization Type</span>
                          <ul>
                            <li>Enterprise</li>
                            <li>Startups</li>
                          </ul>
                        </li>
                      </ul>
                </CollapsibleList>
            </div>
            <div class='items' id='dev'>
                <CollapsibleList>
                    <span slot='header' class='items__title'>Developers</span>
                    <ul slot='content'>
                        <li>
                            <span class='items__grp-title'>Technologies Documentation</span>
                        <ul>
                            <li>React</li>
                            <li>Angular</li>
                            <li>Vue</li>
                            <li>IOS Swift</li>
                            <li>Android Kotlin</li>
                            <li>Android Java</li>
                            <li>React Native</li>
                            <li>Ionic/Capacitor</li>
                            <li>WordPress</li>
                            <li>Laravel/PHP</li>
                            <li>Flutter</li>
                            <li>Next.js</li>
                        </ul>
                        </li>
                        <li>
                            <span  class='items__grp-title'>Documentation</span>
                        <ul>
                            <li>Product updates</li>
                            <li>Tutorials</li>
                            <li>Open-source Apps</li>
                            <li>Product status</li>
                            <li>Glossary</li>
                        </ul>
                        </li>
                    </ul>
                </CollapsibleList>
            </div>
            <div class='items' id='resources'>
                <CollapsibleList>
                    <span slot='header' class='items__title'>Resources</span>
                    <ul slot='content'>
                        <li>Customer stories</li>
                        <li>Blog</li>
                        <li>Give feedback</li>
                        <li>Community forum</li>
                        <li>Help center</li>
                        <li>Partners</li>
                    </ul>
                </CollapsibleList>
                
            </div>
            <div class='items' id='competitors'>
                <CollapsibleList>
                    <span slot='header' class='items__title'>Competitors</span>
                    <ul slot='content'>
                        <li>SendBird</li>
                        <li>GetStream</li>
                        <li>Applozic</li>
                        <li>Twilio</li>
                        <li>PubNub</li>
                    </ul>
                </CollapsibleList>
                
            </div>
            <div class='items' id='company'>
                <CollapsibleList>
                    <span slot='header' class='items__title'>Company</span>
                    <ul slot='content'>
                        <li>About us</li>
                        <li>Careers</li>
                        <li>Partners</li>
                        <li>Pricing</li>
                        <li>Chat with us</li>
                    </ul>
                </CollapsibleList>
            </div>
        </div>
        <div class=footer>
            <ul class='terms'>
                <li>2023 © CometChat</li>
                <li>Terms of Use</li>
                <li>Privacy Policy</li>
            </ul>
            <ul class='social-media'>
                <li><img src={FacebookIcon} alt='Facebook'/>Facebook</li>
                <li><img src={LinkedInIcon} alt='Linkedin'/>LinkedIn</li>
                <li><img src={InstagramIcon} alt='Instagram'/>Instagram</li>
                <li><img src={TwitterIcon} alt='Twitter'/>Twitter</li>
                <li><img src={GithubIcon} alt='Github'/>Github</li>
            </ul>
        </div>
    </div>
</section>

<style lang="scss">
    .section {
        padding: 0 4rem;
        background-image: url('../../assets/icons/stars.svg');
        background-position: center top;
        background-repeat: no-repeat;
    }
    .container {
        width: 100%;
        max-width: 1200px;
        margin: 0 auto;
    }
    .footer {
        display: flex;
        margin: 3rem auto;
        font-size: 1.4rem;

        .social-media, .terms {
            max-width: 100%;
            display: flex;
            gap: 2rem;
            flex-wrap: wrap;
        }
        .social-media {
            margin-left: auto;
            li {
                display: flex;
                align-items: center;
                gap: .5rem;
            }
        }
    }
    .items-list {
        width: 100%;
        display: grid;
        grid-template-areas:
            "tech solutions dev resources"
            "tech solutions dev competitors"
            "tech . dev company"
            "tech . . .";
        justify-content: space-between;
        margin: 8rem auto;
    }
    #tech {
        grid-area: tech;
    }

    #solutions {
        grid-area: solutions;
    }

    #dev {
        grid-area: dev;
    }
    
    #resources {
        grid-area: resources;
    }
    
    #competitors {
        grid-area: competitors;
    }

    #company {
        grid-area: company;
    }

    .items {
        li {
            margin-top: 0.8rem;
        }
        &__title {
            color: rgba(104, 82, 214, 1);
        }

        &__grp-title {
            display: inline-block;
            margin-top: 1rem;
            opacity: 0.55;

        }
    }
    
    ul { 
        list-style: none; 
    }

    @media screen and (max-width: 940px) {
        .items-list {
           display: flex;
           flex-direction: column;;
        }
    }

    @media screen and (max-width: 890px) {
        .footer {
           flex-direction: column-reverse;
           align-items: center;

           .social-media {
                margin-left: 0;
            }

            .social-media, .terms {
                gap: 1rem;
                margin: 1rem;
            }
        }

        
    }
</style>