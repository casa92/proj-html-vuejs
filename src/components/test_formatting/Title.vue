<template>
    <div class="section-title">
        <h2>{{ title }}</h2>
        <h3>{{ subTitle }}</h3>
        
    </div>
</template>

<script>


export default {
    name: "Title",
    props: [ 'title', 'subTitle' ],
}
</script>

<style lang="scss" scoped>
    @import '../../style/variables.scss';

   .section-title {
       margin: auto;
       text-align: center;
       max-width: 480px;
       padding: $padding_section;

       h2 {
           font-family: $title_font;
           color: $title_color;
           font-size: 40px;
           font-weight: 400;
           margin-bottom: 2px;
       }
       h3 {
           font-size: 24px;
           font-weight: 600;
       }
   }
</style>
