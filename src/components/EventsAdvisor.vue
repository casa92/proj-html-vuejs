<template>
    <div class="event-advisor">
        <div class="container">
            <div class="flex-container">
                <div class="advice">
                    Starts TOMORROW! Our biggest event of the year...
                </div>
                <div class="countdown">
                    <div>
                        <i class="far fa-clock"></i>
                    </div>
                    <div>
                        00 : 00: 00 : 00
                    </div>
                </div>
                <div class="btn-header">
                    <a href="#">
                        Get ticket
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>


export default {
    name: "EventAdvisor",
}
</script>

<style lang="scss" scoped>
    @import '../style/variables.scss';

    .event-advisor {
        background-color: #f5f5f5;
        height: 36px;
        line-height: 35px;

        .container {
            width: 90%;
            margin: auto;
            font-size: 10px;
            
            .flex-container {
                display: flex;
                justify-content: center;
                align-items: center;

                & > div {
                    margin-right: 25px;
                }

                .btn-header {
                    
                    display: inline-block;
                    border-radius: 5px;
                    font-size: 10px;
                    font-weight: 700;
                    line-height: normal;
                    z-index: 100;
                    background-color: $btn_primary_color;

                    a {
                        display: inline-block;
                        padding: 5px 26px;
                        color: #fff;        
                    }
                    &-primary-color {
                        background-color: $btn_primary_color;
                        color: #fff;
                    }
                    &:hover {
                        background-color: $btn_prymary_hover;
                        color: #fff;
                    }
                }
                .countdown {
                    display: flex;
                    font-size: 14px;
                    font-weight: 700;

                    i {
                        font-size: 13px;
                        margin-right: 6px;
                    }
                }
            }
        }
    }
</style>
