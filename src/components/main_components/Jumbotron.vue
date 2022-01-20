<template>
    <section class="jumbotron">
        <div class="left-side">
            <!-- forma di sfondo -->
            <img src="../../assets/img/artist-shape-02-600x324.png" alt="">
            <!-- macchia azzurra -->
            <img src="../../assets/img/macchia-light-blue.svg" alt="">
            <!-- puntini -->
            <img src="../../assets/img/artist-shape-03.png" alt="">
            <!-- testa -->
            <img src="../../assets/img/artist-hero-image-03.png" alt="">
            <!-- quadro pittura -->
            <img src="../../assets/img/artist-hero-image-02-232x300.jpg" alt="">
            <!-- quadro scimmia -->
            <img src="../../assets/img/artist-hero-image-01.jpg" alt="">
        </div>
        <div class="right-side">
            <!-- forma di sfondo -->
            <img src="../../assets/img/artist-shape-01-300x288.png" alt="">
            <!-- foglia -->
            <img src="../../assets/img/artist-shape-04.png" alt="">
            <!-- pennello -->
            <img src="../../assets/img/artist-shape-05.png" alt="">
             <!-- forma a puntini -->
            <img src="../../assets/img/maxcoach-shape-12-100x100.png" alt="">
            <!-- macchia di colore -->
            <img src="../../assets/img/macchia-blu.svg" alt="">
            <!-- foto artista  -->
            <img src="../../assets/img/artist-hero-image-04.jpg" alt="">
           


        </div>

        <!-- titolo -->
        <div class="title">
            <h2>Hello, Im Matin</h2>
            <h3>Artist Coaching And Mentoring Might Be for You</h3>

            <!-- button -->
            <div class="btn-main btn-main-primary-color">
                <a href="#">Get started today</a>
            </div>
        </div>
        
    </section>
</template>

<script>
export default {
    name: "Jumbotron",
}
</script>

<style lang="scss" scoped>
    
    @import '../../style/variables.scss';

    .jumbotron {
        width: 100%;
        position: relative;

        height: 510px;
        background-color: #fbf9f6;

        img {
            position: absolute;
        }

        .title {
            position: absolute;
            width: 380px;
            text-align: center;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 22px;

            h2 {
                font-family: $title_font;
                font-weight: 700;
                color: #69a0fd;
                font-size: 40px;
            }
            h3 {
                margin-bottom: 25px;
                font-weight: 700;
            }
        }

        .left-side {
            width: 50%;
            float: left;
            position: relative;

            img {
                //forma di sfondo
                &:nth-child(1) {
                    width: 95%;
                    left: 0;
                    top: 0;
                }
                //macchia azzurra
                &:nth-child(2) {
                    width: 500px;
                    max-height: 461px;
                    left: -130px;
                    top: 80px;
                }
                //puntini
                &:nth-child(3) {
                    width: 240px;
                    top: 99px;
                    left: 5px;
                }
                //testa
                &:nth-child(4) {
                    width: 160px;
                    top: 250px;
                    left: 321px;
                }
                //quadro pittura
                &:nth-child(5) {
                    width: 190px;
                    top: 70px;
                    left: 230px;
                }
                //quadro scimmia
                &:nth-child(6) {
                    width: 142px;
                    top: 290px;
                    left: 94px;
                }

            }
        }
        .right-side {
            width: 50%;
            height: inherit;
            float: right;
            position: relative;

            img {
                //forma di sfondo
                &:nth-child(1) {
                    width: 475px;
                    right: 110px;
                    top: 0;
                }
                //foglia
                &:nth-child(2) {
                    width: 85px;
                    right: 107px;
                    top: 65px;
                }
                //pennello
                &:nth-child(3) {
                    width: 230px;
                    right: 65px;
                    bottom: 0;
                }
                //forma a puntini
                &:nth-child(4) {
                    width: 120px;
                    right: 240px;
                    bottom: 25px;
                }
                //forma a puntini
                &:nth-child(5) {
                    width: 120px;
                    right: 295px;
                    bottom: 40px;
                }
                //foto artista
                &:nth-child(6) {
                    width: 215px;
                    right: 160px;
                    bottom: 35px;
                }
               
            }
        }

    }
</style>