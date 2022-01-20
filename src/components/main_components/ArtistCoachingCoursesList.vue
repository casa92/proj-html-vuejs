<template>
    <section class="latest-courses">
        <Title title="Artist coaching" subTitle="Latest Online Courses"/>
        <div class="courses-list">
            <!-- <div class="course-card">
                <div class="course-card-image">
                    <img src="../../assets/img/artist-course-08-480x480.jpg" alt="">
                </div>
                <div class="course-card-description">
                    <div class="price">
                        $18.00
                    </div>
                    <div class="title">
                        The Acrylic Painting Accademy
                    </div>
                    <div class="features">
                        <div class="lessons">
                            <i class="far fa-file-alt"></i>
                            4 lessons
                        </div>
                        <div class="students">
                            <i class="far fa-user"></i>
                            50 Students
                        </div>
                    </div>   
                </div>
            </div>
            <div class="course-card">
                <div class="course-card-image">
                    <img src="../../assets/img/artist-course-08-480x480.jpg" alt="">
                </div>
                <div class="course-card-description">
                    <div class="price">
                        $18.00
                    </div>
                    <div class="title">
                        The Acrylic Painting Accademy
                    </div>
                    <div class="features">
                        <div class="lessons">
                            <i class="far fa-file-alt"></i>
                            4 lessons
                        </div>
                        <div class="students">
                            <i class="far fa-user"></i>
                            50 Students
                        </div>
                    </div>   
                </div>
            </div>
            <div class="course-card">
                <div class="course-card-image">
                    <img src="../../assets/img/artist-course-08-480x480.jpg" alt="">
                </div>
                <div class="course-card-description">
                    <div class="price">
                        $18.00
                    </div>
                    <div class="title">
                        The Acrylic Painting Accademy
                    </div>
                    <div class="features">
                        <div class="lessons">
                            <i class="far fa-file-alt"></i>
                            4 lessons
                        </div>
                        <div class="students">
                            <i class="far fa-user"></i>
                            50 Students
                        </div>
                    </div>   
                </div>
            </div>
            <div class="course-card">
                <div class="course-card-image">
                    <img src="../../assets/img/artist-course-08-480x480.jpg" alt="">
                </div>
                <div class="course-card-description">
                    <div class="price">
                        $18.00
                    </div>
                    <div class="title">
                        The Acrylic Painting Accademy
                    </div>
                    <div class="features">
                        <div class="lessons">
                            <i class="far fa-file-alt"></i>
                            4 lessons
                        </div>
                        <div class="students">
                            <i class="far fa-user"></i>
                            50 Students
                        </div>
                    </div>   
                </div>
            </div>

            <div class="course-card">
                <div class="course-card-image">
                    <img src="../../assets/img/artist-course-08-480x480.jpg" alt="">
                </div>
                <div class="course-card-description">
                    <div class="price">
                        $18.00
                    </div>
                    <div class="title">
                        The Acrylic Painting Accademy
                    </div>
                    <div class="features">
                        <div class="lessons">
                            <i class="far fa-file-alt"></i>
                            4 lessons
                        </div>
                        <div class="students">
                            <i class="far fa-user"></i>
                            50 Students
                        </div>
                    </div>   
                </div>
            </div>
            <div class="course-card">
                <div class="course-card-image">
                    <img src="../../assets/img/artist-course-08-480x480.jpg" alt="">
                </div>
                <div class="course-card-description">
                    <div class="price">
                        $18.00
                    </div>
                    <div class="title">
                        The Acrylic Painting Accademy
                    </div>
                    <div class="features">
                        <div class="lessons">
                            <i class="far fa-file-alt"></i>
                            4 lessons
                        </div>
                        <div class="students">
                            <i class="far fa-user"></i>
                            50 Students
                        </div>
                    </div>   
                </div>
            </div>
            <div class="course-card">
                <div class="course-card-image">
                    <img src="../../assets/img/artist-course-08-480x480.jpg" alt="">
                </div>
                <div class="course-card-description">
                    <div class="price">
                        $18.00
                    </div>
                    <div class="title">
                        The Acrylic Painting Accademy
                    </div>
                    <div class="features">
                        <div class="lessons">
                            <i class="far fa-file-alt"></i>
                            4 lessons
                        </div>
                        <div class="students">
                            <i class="far fa-user"></i>
                            50 Students
                        </div>
                    </div>   
                </div>
            </div> -->
            <div v-for="(singleCard, index) in coursesCards" class="course-card" :key="index">
                <div class="course-card-image">
                    <img :src="require(`../../assets/img/${singleCard.courseImg}.jpg`)" alt="">
                </div>
                <div class="course-card-description">
                    <div class="price">
                        $18.00
                    </div>
                    <div class="title">
                        The Acrylic Painting Accademy
                    </div>
                    <div class="features">
                        <div class="lessons">
                            <i class="far fa-file-alt"></i>
                            4 lessons
                        </div>
                        <div class="students">
                            <i class="far fa-user"></i>
                            50 Students
                        </div>
                    </div>   
                </div>
            </div>
        </div>

        <div class="btn-main btn-main-secondary-color">
            <a href="#">
                View all courses
                <i class="fas fa-long-arrow-alt-right"></i>  
            </a>  
        </div>
    </section>
</template>

<script>
import Title from '../test_formatting/Title.vue';

export default {
    name: "ArtistCoachingCoursesList",
    components: {
        Title,
    },
    data: function() {
        return {
            coursesCards: [
                {   id: '1',
                    courseImg: 'artist-course-08-480x480',
                    price: '$18.00',
                    title: 'The Acrylic Painting Accademy',
                    numbOfLessons: '4 lessons',
                    numbOfStudents: '50 Students',
                },
                {   
                    id: '2',
                    courseImg: 'artist-course-07-480x480',
                    price: '$21.00',
                    title: 'Drawing and Shading: Complete Course',
                    numbOfLessons: '14 lessons',
                    numbOfStudents: '50 Students',
                },
                {
                    id: '3',
                    courseImg: 'artist-course-06-480x480',
                    price: '$19.00',
                    title: 'The Color Theory for Digital Artist',
                    numbOfLessons: '7 lessons',
                    numbOfStudents: '50 Students',
                },
                {
                    id: '4',
                    courseImg: 'artist-course-05-480x480',
                    price: '$35.00',
                    title: 'Ultimate Guide to Digital Sketching for Beginner',
                    numbOfLessons: '4 lessons',
                    numbOfStudents: '50 Students',
                },
                {
                    id: '5',
                    courseImg: 'artist-course-04-480x480',
                    price: '$19.00',
                    title: 'Portrait Drawing The Smart Way',
                    numbOfLessons: '2 lessons',
                    numbOfStudents: '50 Students',
                },
                {
                    id: '6',
                    courseImg: 'artist-course-03-480x480',
                    price: '$19.00',
                    title: 'Mastering Watercolor Painting from Beginner',
                    numbOfLessons: '9 lessons',
                    numbOfStudents: '50 Students',
                },
                {
                    id: '7',
                    courseImg: 'artist-course-02-480x480',
                    price: '$25.00',
                    title: 'The Art & Science of Drawing',
                    numbOfLessons: '4 lessons',
                    numbOfStudents: '50 Students',
                },
                {   
                    id: '8',
                    courseImg: 'artist-course-01-480x480',
                    price: '$22.00',
                    title: 'The Colored Pencil Drawing Course',
                    numbOfLessons: '6 lessons',
                    numbOfStudents: '50 Students',
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../../style/variables.scss';

    .latest-courses {
        text-align: center;
        padding-bottom: 70px;
        .courses-list {
            text-align: initial;
            padding: 0 50px;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;

            .course-card {
                width: 20%;
                margin-right: 20px;
                margin-bottom: 35px;

                
                &-description {
                    padding: 12px 22px;
                    font-size: 15px;
                    font-weight: 600;
                    line-height: 23px;

                    .price {
                        font-size: 13px;
                        color: red;
                        font-weight: 800;
                    }
                    .title {
                        margin-top: 5px;
                        margin-bottom: 10px;
                    }
                    .features {
                        color: #797979;
                        font-size: 11px;
                        font-weight: 400;
                        display: flex;
                        .lessons {
                            margin-right: 20px;
                        }
                        i {
                            font-size: 10px;
                            margin-right: 4px;
                        }
                    }
                }
            }
        }
    }  
</style>
