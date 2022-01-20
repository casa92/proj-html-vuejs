<template>
    <header class="container">
        <div class="logo-img">
            <img src="../assets/img/dark-logo.png" alt="">
        </div>
        <nav>
            <ul class="header-menu">
                <!-- <li v-for="(link, index) in exploreMenu" :key="index">
                    <a :href="link.url">
                        {{ link.linkText}}
                    </a>
                </li> -->
                <li v-for="(link, index) in menuLinks" :key="index">
                    <a :href="link.url">
                        {{ link.linkText }}
                        <i class="fas fa-chevron-down"></i>
                    </a>
                </li>
            </ul>
        </nav>
        <div class="social-list">
            <div class="social-icon">
                <a href="#">
                    <i class="fab fa-twitter"></i>
                </a>
            </div>
            <div class="social-icon">
                <a href="#">
                    <i class="fab fa-facebook-f"></i>
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
        
    </header>
</template>

<script>


export default {
    name: "Header",
    data: function() {
        return {
            menuLinks: [
                {
                    id: '1',
                    url: '#',
                    linkText: 'Home'
                },
                {
                    id: '2',
                    url: '#',
                    linkText: 'Pages'
                },
                {
                    id: '3',
                    url: '#',
                    linkText: 'Courses'
                },
                {
                    id: '4',
                    url: '#',
                    linkText: 'Features'
                },
                {
                    id: '5',
                    url: '#',
                    linkText: 'Blog'
                },
                {
                    id: '6',
                    url: '#',
                    linkText: 'Shop'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../style/variables.scss';

    .container {
        width: $width_primary_container;
        margin: auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 60px;

        .logo-img {
            width: 120px;
        }
        .header-menu {
            display: flex;

            li {
                margin-right: 25px;
                font-size: 12px;
                font-weight: 600;


                i {
                    padding-left: 1px;
                    font-size: 7px;
                }
            }
        }
        .social-list {
            display: flex;
            font-size: 13px;
            margin-top: 15px;

            .social-icon {
                color: #797979;
                margin-right: 20px;

                &:hover {
                    color: #ef6f31;
                }
            }
        }
    }

</style>
