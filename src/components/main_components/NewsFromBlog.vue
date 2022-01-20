<template>
    <section class="blog-news">
        <!-- background images -->
        <!-- linea -->
        <img src="../../assets/img/maxcoach-shape-03.png" alt="">
        <!-- cerchio puntinato -->
        <img src="../../assets/img/maxcoach-shape-05.png" alt="">
        <!-- macchia di colore -->
        <img src="../../assets/img/macchia-light-blue.svg" alt="">

        <Title title="Articles and Tips" subTitle="Latest From The Blog"/>
        <div class="article-list">
            <div class="single-article">
                <div class="single-article-features">
                    
                </div>
            </div>
            <div class="single-main-article">
                <img src="../../assets/img/artist-blog-02-500x680.jpg" alt="">
                <div class="single-article-features">
                    
                </div>
            </div>
            <div class="single-article">
                <img src="../../assets/img/artist-blog-01-480x356.jpg" alt="">
                <div class="single-article-features">
                    
                </div>
            </div>
        </div>
        <div class="other-posts">
            Get into details now?
            <a href="#">
                View all posts
                <i class="fas fa-long-arrow-alt-right"></i>
            </a>
        </div>
    </section>
</template>

<script>
import Title from '../test_formatting/Title.vue';


export default {
    name: "NewsFromBlog",
    components: {
        Title,
    }
}
</script>

<style lang="scss" scoped>
    @import '../../style/variables.scss';

    .blog-news {
        background-color: #f5f7fa;
        position: relative;
        padding-bottom: 15s0px;

        & > img {
            // background images
            // linea
            &:nth-child(1) {
                position: absolute;
                width: 100%;
                top: 250px;
            }
            // cerchio puntinato
            &:nth-child(2) {
                position: absolute;
                width: 140px;
                top: 181px;
                left: 435px;
            }
            // macchia di colore
            &:nth-child(3) {
                position: absolute;
                width: 200px;
                top: 570px;
                right: 380px;
            }
        }
        .article-list {
            display: flex;
            justify-content: space-between;
            width: 63%;
            margin: auto;
            
            .single-article {
                width: 195px;
                height: 280px;
                position: relative;
                background-color: #fff;

                img {
                    position: absolute;
                    top: 0;

                }
                &:nth-child(1) {

                    top: 130px;
                    &::after {
                        background-image: url('../../assets/img/artist-blog-03-480x356.jpeg');
                    }
                }
                &:nth-child(3) {
                    top: 45px;
                }
                &::after {
                    content: '';
                    width: 100%;
                    height: 140px;
                    
                    background-position: bottom;
                    background-repeat: no-repeat;
                    background-size: cover;   
                    position: absolute;
                    top: 0;
                    left: 0;
                    
                }
            }
            .single-main-article {
                width: 340px;
                height: 476px;
                margin: 5px 0;
                position: relative;
                

                img {
                    width: 340px;
                }
            }
        }
        .other-posts {
            text-align: center;
            font-size: 13px;
            font-weight: 500;
            margin-top: 60px;
            padding-bottom: $padding_section;
            position: relative;
            a {
                color: #d71f18;
                text-decoration: underline;
                font-weight: 700;

                i {
                    font-size: 13px;
                }
            }
        }

    }


</style>