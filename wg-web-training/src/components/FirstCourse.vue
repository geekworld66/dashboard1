<template>
    <div class="div-wrapper" id="app">
        <div class="div left">
            <div class="div left top">
                <span class="div top-span">当前访客数</span>
                <span class="div bottom-span">2560</span>
            </div>
            <div class="div left bottom">
                <div class="bottom-left-div">
                    <span class="div top-span">在线教师</span>
                    <span class="div bottom-span">102</span>
                </div>
                <div class="bottom-right-div">
                    <span class="div top-span">在线学生</span>
                    <span class="div bottom-span">2408</span>
                </div>
            </div>
        </div>
        <div class="div left">
            <div class="div left top">
                <span class="div top-span">用户总数</span>
                <span class="div bottom-span">38963</span>
            </div>
            <div class="div left bottom">
                <div class="bottom-left-div">
                    <span class="div top-span">总数教师</span>
                    <span class="div bottom-span">869</span>
                </div>
                <div class="bottom-right-div">
                    <span class="div top-span">学生数</span>
                    <span class="div bottom-span">38094</span>
                </div>
            </div>
        </div>
        <div class="div left">
            <div class="div left top">
                <span class="div top-span">课程总数</span>
                <span class="div bottom-span">122</span>
            </div>
            <div class="div left bottom">
                <div class="bottom-left-div">
                    <span class="div top-span">公开课</span>
                    <span class="div bottom-span">86</span>
                </div>
                <div class="bottom-right-div">
                    <span class="div top-span">私有课</span>
                    <span class="div bottom-span">2438</span>
                </div>
            </div>
        </div>
        <div class="div right">
            <div class="div right top">
                <span class="div right-top-span1">活动总数</span>
                <span class="div right-top-span2">4025</span>
            </div>
            <div class="div right bottom">
                <span class="div right-bottom-span1">资源总数</span>
                <span class="div right-bottom-span2">12004</span>
            </div>
        </div>
    </div>
</template>

<script>
    export default {}
</script>

<style lang="scss">
    @mixin make-span($font-size, $height, $width) {
        font-size: $font-size * 1ex;
        height: $height;
        width: $width;
    }

    @mixin make-bottom-div($width, $height, $float) {
        float: $float;
        width: $width;
        height: $height;
        .top-span {
            margin: 10px 0px 10px 15px;
            @include make-span(1, 20%, 80%);
        }
        .bottom-span {
            margin: 0px 0px 10px 15px;
            @include make-span(3, 35%, 80%);
        }
    }

    .div-wrapper{
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        width:800px;
        height:200px;
        background-color: gainsboro;
        margin:0px auto;/*设置外边距上下0px，左右auto，即可实现左右居中的效果*/

        .div{
            background-color: white;
            float:left;
            margin:10px;
            height:170px;

            &.left {
                width:22%;
                border-bottom: 1px solid gainsboro;
                &.top {
                    margin:0%;
                    height: 55%;
                    width: 100%;
                    .top-span {
                        margin:10px 0px 10px 15px;
                        @include make-span(1, 20%, 90%);
                    }
                    .bottom-span {
                        margin: 0px 0px 10px 15px;
                        @include make-span(3, 35%, 90%);
                    }
                }

                &.bottom {
                    margin: 0%;
                    height: 45%;
                    width: 100%;

                    .bottom-left-div {
                        border-right: 1px solid gainsboro;
                        box-sizing: border-box;
                        @include make-bottom-div(50%, 100%, left);
                    }
                    .bottom-right-div {
                        @include make-bottom-div(50%, 100%, right);
                    }
                }
            }

            &.right {
                width: 22%;
                border: none;
                background-color: gainsboro;
                &.top {
                    margin: 0%;
                    width: 100%;
                    height: 45%;
                    background-color: white;

                    .right-top-span1 {
                        margin:10px 15px 10px 15px;
                        @include make-span(1, 15%, 90%);
                    }

                    .right-top-span2 {
                        margin: 0px 15px 10px 15px;
                        @include make-span(3, 30%, 90%);
                    }
                }

                &.bottom {
                    margin: 10% 0px 0px 0px;
                    width: 100%;
                    height: 45%;
                    background-color: white;

                    .right-bottom-span1 {
                        margin: 10px 0px 10px 15px;
                        @include make-span(1, 15%, 90%);
                    }

                    .right-bottom-span2 {
                        margin: 0px 0px 10px 15px;
                        @include make-span(3, 30%, 90%);
                    }
                }
            }
        }
    }
</style>

