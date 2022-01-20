<template>
    <div> 
        <Jumbotron/>
        <ArtistCoachingAbout/>
        <ArtistCoachingCoursesList/>
        <Jumbotron/>
        <Jumbotron/>
    </div>
</template>

<script>

import Jumbotron from './main_components/Jumbotron.vue';
import ArtistCoachingAbout from './main_components/ArtistCoachingAbout.vue';
import ArtistCoachingCoursesList from './main_components/ArtistCoachingCoursesList.vue';

export default {
    name: "Main",
    components: {
        Jumbotron,
        ArtistCoachingAbout,
        ArtistCoachingCoursesList,
    },
}
</script>

<style lang="scss" scoped>

</style>
