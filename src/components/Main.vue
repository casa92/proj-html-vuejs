<template>
    <div> 
        <Jumbotron/>
        <ArtistCoachingAbout/>
        <ArtistCoachingCoursesList/>
        <NewsFromBlog/>
        <UpcomingEvents/>
    </div>
</template>

<script>

import Jumbotron from './main_components/Jumbotron.vue';
import ArtistCoachingAbout from './main_components/ArtistCoachingAbout.vue';
import ArtistCoachingCoursesList from './main_components/ArtistCoachingCoursesList.vue';
import NewsFromBlog from './main_components/NewsFromBlog.vue';
import UpcomingEvents from './main_components/UpcomingEvents.vue';


export default {
    name: "Main",
    components: {
        Jumbotron,
        ArtistCoachingAbout,
        ArtistCoachingCoursesList,
        NewsFromBlog,
        UpcomingEvents,
    },
}
</script>

<style lang="scss" scoped>

</style>
