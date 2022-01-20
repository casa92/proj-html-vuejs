<template>
    <section class="about-section">
        <!-- background images -->
        <!-- prima forma a sinistra -->
        <img src="../../assets/img/artist-shape-01.png" alt="" class="img-shape">
        <!-- macchia di colore -->
        <img src="../../assets/img/macchia-gray.svg" alt="">
        <!-- linea -->
        <img src="../../assets/img/maxcoach-shape-14.png" alt="">
        <!-- cerchio a righe -->
        <img src="../../assets/img/maxcoach-shape-13.png" alt="">
        

        <div class="about-container">
            <!-- title -->
            <Title title="Artist coaching" subTitle="I understand what it takes to create. I can help you with"/>
            <!-- artist coaching about card list -->
            <div class="about-list">
                <div v-for="(singleCard, index) in aboutCards" class="about-list-card" :key="index">
                    <div class="about-list-card-img">
                        <img :src="require(`../../assets/img/${singleCard.image}.png`)" alt="">
                    </div>
                    <h4>{{ singleCard.title }}</h4>
                    <p>{{ singleCard.text }}</p>
                </div>
            </div>
            <!-- quote and mission -->
            <div class="artist-mission">
                <div class="quote">
                    <div>
                        <img src="../../assets/img/artist-quote-icon.png" alt="">
                    </div>
                    <div class="quote-text">
                        I coach and mentor visual artists, like you, to Create Like You Mean It
                    </div>
                    <div class="quote-author">
                        Martin Garrix
                    </div>
                </div>
                <div class="mission">
                    <p>
                        As a coach and mentor, my ultimate goal is to motivate visual artists toward inspired action. I help you get you back on track to being the productive, creative, meaningful and authentic artist you truly want to be. I support artists in craftingand living a creative life as well as feeling good about themselves and their art.
                        <br><br>
                        As an artist and educator for nearly 30 years, I understand what it takes to create.
                    </p>
                    <div class="btn-main btn-main-secondary-color">
                        <a href="#">Get started today</a>
                    </div>
                </div>
            </div>
            
        </div>
        <!-- video -->
        <div class="about-video">
            <img src="../../assets/img/artist-video-poster.jpg" alt="">
        </div>
        <div class="waves">
            <div class="svg">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="#faf8f6" fill-opacity="1" d="M0,64L30,96C60,128,120,192,180,197.3C240,203,300,149,360,128C420,107,480,117,540,144C600,171,660,213,720,197.3C780,181,840,107,900,64C960,21,1020,11,1080,53.3C1140,96,1200,192,1260,192C1320,192,1380,96,1410,48L1440,0L1440,320L1410,320C1380,320,1320,320,1260,320C1200,320,1140,320,1080,320C1020,320,960,320,900,320C840,320,780,320,720,320C660,320,600,320,540,320C480,320,420,320,360,320C300,320,240,320,180,320C120,320,60,320,30,320L0,320Z"></path></svg>
            </div>
        </div>
        <!-- testimonials -->
        <div class="testimonials">
            <Title title="Testimonials" subTitle="Why do people love me?"/>
            <div class="testimonials-list">
                <div v-for="(testimonial, index) in testimonialsCards" class="single-review" :key="index">
                    <h4>{{ testimonial.title}}</h4>
                    <p>{{ testimonial.text}}</p>
                    <div class="single-review-user-info">
                        <div class="user-img">
                            <img :src="require(`../../assets/img/${testimonial.avatarImage}.jpg`)" alt="">
                        </div>
                        <div class="user-data">
                            <div class="name">
                                {{testimonial.name}}
                            </div>
                            <div class="profession">
                                {{testimonial.profession}}
                            </div>

                        </div>
                    </div>
                </div>
            </div>
            <div class="image-selector">
                <div class="point point-active">
                    
                </div>
                <div class="point">
                    
                </div>
                <div class="point">
                    
                </div>
                <div class="point">
                    
                </div>
            </div>
        </div>
        

    </section>
</template>

<script>
import Title from '../test_formatting/Title.vue';

export default {
    name: "ArtistCoachingAbout",
    components: {
        Title,
    },
    data: function() {
        return {
            aboutCards : [
                {
                    image: 'artist-box-image-01',
                    title: 'Online Courses',
                    text: 'Online art coaching now offers you a very powerful way to redesign your artist mind.'
                },
                {
                    image: 'artist-box-image-02',
                    title: 'One to One',
                    text: 'Getting the necessary clarity about the current state to help you improve your ability.'
                },
                {
                    image: 'artist-box-image-03',
                    title: 'Anywhere',
                    text: 'Access to valuable and portable program which allow you to setup and live anywhere you want.'
                },
                {
                    image: 'artist-box-image-04',
                    title: 'On Time',
                    text: 'Punctuality is our top priority because it\'s an essential criteria to assess a program quality'
                }
            ],
            testimonialsCards : [
                {
                    title: 'It\'s a choice of quality for people with special needs',
                    text: 'I\'m very strict person so I require everything to be organized and neat. Then, I\'ll be able to make things right and shine. MaxCoach guys just got me.',
                    avatarImage: 'artist-testimonial-avatar-02',
                    name: 'Florence Themes',
                    profession: '/ Multimedia Admin'
                },
                 {
                    title: 'High level of efficiency and scientific teaching methods',
                    text: 'I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from the syllabus. Great study portal for people like me.',
                    avatarImage: 'artist-testimonial-avatar-04',
                    name: 'Mina Hollace',
                    profession: '/ Freelancer'
                },
                {
                    title: 'Professional team of specialists and passionate mentors at reach',
                    text: 'I need to get a certification for English proficiency and MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.',
                    avatarImage: 'artist-testimonial-avatar-01',
                    name: 'Madley Pondor',
                    profession: '/ IT Specialist'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../../style/variables.scss';

    .about-container {
        width: 63%;
        margin: auto;
    }
    .about-section {
        position: relative;

        .waves {
            // display: flex;
            // display: inline-block;

            .svg {
                
                width: 120%;
                height: 200px;
                margin-top: -180px;
            }
        }
        & > img {
            //prima forma a sinistra
            &:nth-child(1) {
                transform: rotate(-130deg);
                position: absolute;
                top: 45px;
                left: -120px;
                width: 485px;
            }
            //macchia di colore
            &:nth-child(2) {
                position: absolute;
                width: 300px;
                top: 150px;
                right: 170px;
            }
            //linea
            &:nth-child(3) {
                position: absolute;
                width: 100%;
                top: 80px;
               
            }
            //cerchio a righe
            &:nth-child(4) {
                position: absolute;
                width: 130px;
                top: 160px;
                right: -40px;
            }
        
        }
        .about-list {
            position: relative;
            display: flex;
            justify-content: space-between;


            &-card {
                width: 187px;
                font-weight: 200;
                font-size: 11px;

                &:nth-child(4) {
                    h4 {
                        margin-top: 17px;
                    }
                }

                h4 {
                    font-size: 14px;
                    font-weight: 500;
                    margin: 10px 0;
                }
                &:nth-child(2n) {
                    position: relative;
                    top: 40px;
                }

                &-img {
                    width: 100px;

                    img {
                        max-height: 80px;
                    }
                }
            }
        }
        .artist-mission {
            padding-top: 140px;
        
            display: flex;
            justify-content: space-between;

            .quote {
                width: 40%;
                // margin-left: 10px;
                text-align: center;

                img {
                    width: 30px;
                    padding-bottom: 10px;
                }
                &-text {
                    font-size: 36px;
                    font-weight: 600;
                }
                &-author {
                    margin-top: 20px;
                    font-family: $title_font;
                    color: $title_color;
                    font-weight: 700;
                    font-size: 35px;
                }
            }
            .mission {
                width: 49%;
                font-weight: 300;
                font-size: 13px;
                line-height: 22px;
                margin-top: 50px;

                p {
                    margin-bottom: 20px;
                }

            }
        }
        .about-video {
            text-align: center;
            margin-top: 130px;
            position: relative;

            img {
                width: 650px;
            }

        }
        .testimonials {
            background-color: #faf8f6;
            margin-top: 11px;
            padding-bottom: 70px;

            .testimonials-list {
                display: flex;
                justify-content: space-evenly;

                .single-review {
                
                    width: 30%;
                    padding: 30px;
                    line-height: 20px;
                    background-color: #fff;
                    position: relative;

                    h4 {
                        font-size: 14px;
                        margin-bottom: 12px;
                    }
                    p {
                        font-size: 13px;
                    
                    }
                    &-user-info {
                        margin-top: 30px;
                        display: flex;
                        padding-bottom: 15px;

                        .user-img {
                            width: 50px;
                            
                            img {
                                border-radius: 50%;
                            }
                        }
                        .user-data {
                            margin-left: 15px;
                            font-size: 12px;

                            .name {
                                font-weight: 700;
                            }
                        }
                    }
                    &::after {
                        content: '';
                        width: 100%;
                        height: 100%;
                        background-color: rgba($color: #fff, $alpha: 0.6);
                        position: absolute;
                        top: 0;
                        left: 0;
                    }
                    &:hover {
                        &::after {
                            background-color: transparent;
                        }
                    }
                }
            }
            .image-selector {
                display: flex;
                justify-content: center;
                align-items: center;
                margin-top: 40px;

                .point {
                    margin: 0 8px;
                    height: 6px;
                    width: 6px;
                    background-color: lightgray;
                    border-radius: 50%;

                    &-active {
                        height: 9px;
                        width: 9px;
                        
                        background-color: black;
                    }
                    
                }
            }

        }
    }
</style>
