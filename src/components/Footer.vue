<template>
    <footer>
        <div class="newsletter">
            <!-- img sinistra -->
            <img src="../assets/img/artist-shape-color-paint-top-left.png" alt="">
            <!-- img destra -->
            <img src="../assets/img/artist-shape-color-paint-bottom-right.png" alt="">
            <div class="newsletter-input-container">
                <div class="newsletter-goal">
                    Newsletter to get in touch
                </div>
                <div class="newsletter-input">
                    <input type="email" placeholder="Your e-mail">
                    <i class="fas fa-long-arrow-alt-right"></i>
                </div>
            </div>
        </div>

        <div class="footer-bottom">
            <div class="container">
                <div class="address">
                    <h5>Address</h5>
                    <div>
                        382 NE 191st St # 87394 Miami, FL 33179-3899 <br>
                        +1(305) 547-9909 (9am - 5pm EST, Monday - Friday) <br>
                        support@maxcoach.com
                    </div>
                    <div class="social-list">
                        <div class="social-icon">
                            <a href="#">
                                <i class="fab fa-facebook-square"></i>
                            </a>
                        </div>
                        <div class="social-icon">
                            <a href="#">
                                <i class="fab fa-twitter"></i>
                            </a>
                        </div>
                        <div class="social-icon">
                            <a href="#">
                                <i class="fab fa-instagram"></i>
                            </a>
                        </div>
                        <div class="social-icon">
                            <a href="#">
                                <i class="fab fa-linkedin"></i>
                            </a>
                        </div>
                    </div>
                </div>

                <div class="explore">
                    <h5>Explore</h5>
                    <nav>
                        <ul>
                            <li v-for="(link, index) in exploreMenu" :key="index">
                                <a :href="link.url">
                                    {{ link.linkText}}
                                </a>
                            </li>
                        </ul>
                    </nav>
                </div>

                <div class="Information">
                    <h5>Explore</h5>
                    <nav>
                        <ul>
                            <li v-for="(link, index) in informationMenu" :key="index">
                                <a :href="link.url">
                                    {{ link.linkText}}
                                </a>
                            </li>
                        </ul>
                    </nav>
                </div>

                <div class="Instagram">
                    <h5>Instagram</h5>
                    <span> @maxcoach</span>
                    <div class="img-gallery">
                        <div class="single-image">
                            <img src="../assets/img/120084500_197897808368764_8114555493043279565_n.jpg" alt="">
                        </div>
                        <div class="single-image">
                            <img src="../assets/img/120012142_177596140500760_8623485824101406058_n.jpg" alt="">
                        </div>
                        <div class="single-image">
                            <img src="../assets/img/120099363_364334431619755_7198812647386067017_n.jpg" alt="">
                        </div>
                    </div>
                </div>
                
            </div>
            <div class="credits">
                &copy; 2020 Maxcoach. All Rights Reserved
            </div>
        </div>
        
    </footer>
</template>

<script>


export default {
    name: "Footer",
    data: function() {
        return {
            exploreMenu: [
                {
                    id: '1',
                    url: '#',
                    linkText: 'Start here'
                },
                {
                    id: '2',
                    url: '#',
                    linkText: 'Success story'
                },
                {
                    id: '3',
                    url: '#',
                    linkText: 'Blog'
                },
                {
                    id: '4',
                    url: '#',
                    linkText: 'Courses'
                },
                {
                    id: '5',
                    url: '#',
                    linkText: 'Contact us'
                }
            ],
            informationMenu: [
                {
                    id: '1',
                    url: '#',
                    linkText: 'Membership'
                },
                {
                    id: '2',
                    url: '#',
                    linkText: 'Purchase guide'
                },
                {
                    id: '3',
                    url: '#',
                    linkText: 'Privacy policy'
                },
                {
                    id: '4',
                    url: '#',
                    linkText: 'Terms of services'
                }
            ]
            
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../style/variables.scss';

    .newsletter {
        height: 140px;
        background-color: #224184;
        position: relative;
        color: #fff;

        img {
            &:nth-child(1) {
                position: absolute;
                left: 0;
                bottom: 0;
                height: 100%;
            }
            &:nth-child(2) {
                position: absolute;
                right: 0;
                bottom: 0;
                height: 90%;
            }
        }
        &-input-container {
            width: 60%;
            height: inherit;
            margin: auto;
            display: flex;
            justify-content: space-between;
            align-items: center;

            .newsletter-goal {
                font-family: Georgia, 'Times New Roman', Times, serif;
                font-size: 25px;
                font-weight: 500;
                width: 25%;
                text-align: right;
                margin-right: 85px;
            }
            .newsletter-input {
                flex-grow: 1;

                input {
                    background-color: transparent;
                    font-size: 18px;
                    font-weight: 300;
                    
                    border: none;
                    border-bottom: 1px solid #917b7b;
                    padding-right: 0px;
                    padding-bottom: 8px;
                    width: 90%;
                    color: #fff;
                    &::placeholder {
                        color: #fff;
                    }
                    &:focus {
                        outline: none;
                    }
                }
                i { 
                    vertical-align: middle;
                    position: relative;
                    right: 20px;
                    font-size: 18px;
                }
            }
        }
    }

    .footer-bottom {
        padding-top: 65px;
        padding-bottom: 40px;
        font-size: 10px;
        

        h5 {
            font-size: 13px;
            margin-bottom: 3px;
        }

        .container {
            width: $width_primary_container;
            margin: auto;
            line-height: 25px;
            display: flex;
            justify-content: space-between;

            .address {
            
                .social-list {
                    display: flex;
                    font-size: 17px;
                    margin-top: 15px;

                    .social-icon {
                        color: #bcbcbc;
                        margin-right: 20px;

                        &:hover {
                            color: #224184;
                        }
                    }
                }

            }
            .Instagram {
                h5 {
                    display: inline-block;
                }
                span {
                    font-size: 11px;
                    color: #d71f18;
                }
                .img-gallery {
                    margin-top: 15px;
                    display: flex;

                    .single-image {
                        width: 100px;
                        margin-right: 15px;

                        img {
                            width: 95px;
                        }
                    }
                }
            }
        }
        .credits {
            text-align: center;
            margin-top: 80px;
            font-size: 10px;
            font-weight: 500;
            color: #bcbcbc;
        }
    }
</style>


