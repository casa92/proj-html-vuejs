<template>
    <div class="upcoming-events">
        <Title title="Upcoming Events" subTitle="Let's Work Together"/>
        <div class="container">
            <div class="events-list">
                <div v-for="(singleCard, index) in eventsCards" class="single-event" :key="index">
                    <div class="single-event-image">
                        <img :src="require(`../../assets/img/${singleCard.eventImg}.jpg`)" alt="">
                    </div>
                    <div class="single-event-feature">
                        <div class="date">
                            {{ singleCard.date }}
                        </div>
                        <div class="title">
                            {{ singleCard.title }}
                        </div>
                        <div class="where">
                            <i class="fas fa-map-marker-alt"></i>
                            {{ singleCard.where }}
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
    </div>
</template>

<script>
import Title from '../test_formatting/Title.vue';

export default {
    name: "UpcomingEvents",
    components: {
        Title,
    },
    data: function() {
        return {
            eventsCards: [
                {
                    id: '1',
                    eventImg: 'artist-event-04-250x300',
                    date: 'NOV 22, 2020',
                    title: 'Storytelling Workshop',
                    where: 'Texas, US'
                },
                {
                    id: '2',
                    eventImg: 'artist-event-03-250x300',
                    date: 'OCT 10, 2020',
                    title: 'Painting Art Contest 2020',
                    where: 'New York, US'
                },
                {
                    id: '3',
                    eventImg: 'artist-event-02-250x300',
                    date: 'NOV 23, 2020',
                    title: 'International Art Fair 2020',
                    where: 'Hamburg, Germany'
                },
                {
                    id: '4',
                    eventImg: 'artist-event-01-250x300',
                    date: 'DEC 15, 2020',
                    title: 'Street Performance: Call for Artist',
                    where: 'Illinois, US'
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

    .upcoming-events {

        .container {
            width: 63%;
            margin: auto;
            .events-list {
                display: flex;
                flex-wrap: wrap;
                justify-content: space-between;

                .single-event {
                    display: flex;
                    align-items: center;
                    margin-bottom: 45px;
                    width: 49%;

                    &:nth-child(3) {
                        flex-direction: row-reverse;

                        .single-event-feature {
                            text-align: right;
                            margin-left: 0;
                            margin-right: 30px;
                        }
                    }
                    &:nth-child(4) {
                        flex-direction: row-reverse;

                        .single-event-feature {
                            text-align: right;
                            margin-left: 0;
                            margin-right: 30px;
                        }
                    }
                    img {
                        width: 180px;
                        height: 210px;
                    }
                    .single-event-feature {
                        margin-left: 30px;

                        .date {
                            font-size: 13px;
                            color: #797979;
                        }
                        .title {
                            font-size: 14px;
                            font-weight: 700;
                            margin: 5px 0;
                        }
                        .where {
                            margin-top: 12px;
                            font-size: 10px;
                            font-weight: 300;
                            color: #797979;

                            i {
                                margin-right: 4px;
                            }
                        }
                    }
                    
                }
            }
        }
    }
</style>
