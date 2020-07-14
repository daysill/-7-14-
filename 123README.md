# -7-14-<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>刘旭-7.14</title>
    <style>
        * {
            margin: 0px;
            padding: 0px;
        }

        .box {
            width: 300px;
            height: 200px;
            border: 1px solid darkcyan;
        }

        .title {
            width: 100%;
            height: 30px;
            background-color: #ccc;
        }

        .title a {
            float: left;
            width: 25%;
            line-height: 30px;
            text-align: center;
            text-decoration: none;
        }

        .con {
            width: 100%;
            height: 170px;
        }

        .con-list {
            width: 100%;
            height: 100%;
            display: none;
        }

        .container {
            width: 484px;
            height: 301px;
            position: relative;
        }

        .container-con {
            width: 462px;
            height: 282px;
            margin: 10px;
            box-shadow: 0 2px 8px 0 rgba(0, 0, 0, .09);
        }

        .con-list3 {
            width: 100%;
            height: 57px;
            background: #f1f1f1;
        }

        .con-list1 {
            float: left;
            color: #000;
            height: 57px;
            width: 50%;
            font-size: 18px;
            cursor: pointer;
            line-height: 57px;
            text-align: center;

        }

        .con-foot-a {
            height: 225px;
            width: 462px;
            display: none;
        }

        .con-foot-b {
            height: 225px;
            width: 462px;
            display: block;

        }

        .con-foot-c {
            position: absolute;
            top: 143px;
            height: 87px;
            width: 291px;
            background-repeat: no-repeat;
            background-position: 0 center;
            background-color: rgba(0, 0, 0, 0);
            background-image: url(https://img.alicdn.com/tfs/TB1AnTXewMPMeJjy1XcXXXpppXa-290-87.png);
            z-index: 99;
        }

        .con-foot-c-1 {
            margin-left: 26px;
            margin-top: 15px;
            vertical-align: middle !important;
        }

        .con-con1 {
            width: 23px;
            height: 23px;

        }

        .con-span {
            margin-left: 8px;
            font-size: 24px;
            font-weight: 700;
            letter-spacing: 1px;
            color: #00B262;
        }

        .con-span2 {
            margin-left: 26px;
            font-size: 20px;
            letter-spacing: 1px;
            color: black;
        }

        .item {
            float: right;
            margin-top: 10px;
            margin-right: 30px;
            width: 200px;
            height: 200px;
        }
    </style>

</head>

<body>
    <div class="box">
        <div class="title">
            <a href="javascript:;" style="background: red;">选项一</a>
            <a href="javascript:;">选项二</a>
            <a href="javascript:;">选项三</a>
            <a href="javascript:;">选项四</a>
        </div>
        <div class="con">
            <div class="con-list" style="display: block;">111111</div>
            <div class="con-list">122211</div>
            <div class="con-list">113311</div>
            <div class="con-list">114411</div>
        </div>
    </div>
    <div class="container">
        <div class="container-con">
            <div class="con-list3">
                <div class="con-list1" style="color:#fff;background-color: #00B262;">今日疯抢</div>
                <div class="con-list1">量贩装</div>
            </div>
            <div class="con-foot">
                <div class="con-foot-a" style="display: block;">
                    <a href="javascript:;" class="con-foot-b">
                        <div class="con-foot-c">
                            <div class="con-foot-c-1">
                                <img src="https://img.alicdn.com/tfs/TB12RqQewMPMeJjy1XdXXasrXXa-23-23.png" alt=""
                                    class="con-con1">
                                <span class="con-span">欢乐零食购</span>
                            </div>
                            <div>
                                <span class="con-span2">爆款直降</span>
                            </div>
                        </div>
                        <img src=" https://img.alicdn.com/tfs/TB1_O_LgSrqK1RjSZK9XXXyypXa-400-400.jpg" alt=""
                            class="item">
                    </a>
                </div>
                <div class="con-foot-a">
                    <a href="javascript:;" class="con-foot-b">
                        <div class="con-foot-c">
                            <div class="con-foot-c-1">
                                <img src="https://img.alicdn.com/tfs/TB12RqQewMPMeJjy1XdXXasrXXa-23-23.png" alt=""
                                    class="con-con1">
                                <span class="con-span">爆款直降</span>
                            </div>
                            <div>
                                <span class="con-span2">粮油调味</span>
                            </div>
                        </div>
                        <img src="https://img.alicdn.com/tfs/TB1jNScP6TpK1RjSZKPXXa3UpXa-400-400.jpg" alt=""
                            class="item">
                    </a>
                </div>
            </div>
        </div>
    </div>
    <script>
        var links = document.querySelectorAll(".title a");
        var lists = document.querySelectorAll(".con-list");
        console.log(links);
        console.log(lists);
        for (let i = 0; i < links.length; i++) {
            // links[i].index = i; //1 . 对象存储属性值
            // console.log(links[i].index);
            // links[i].onlick = function () {
            //     console.log(this.index);
            // }
            //2.闭包  函数就是让局部变量存储在内存当中
            // (function（i） {var
            //     links[i].onlick = function () {
            //         alert(i);
            //     }
            // })(i);
            //3.
            //let
            console.log(links[i]);

            links[i].onclick = function () {
                for (let j = 0; j < lists.length; j++) {
                    console.log(j);
                    lists[j].style.display = "none";
                    links[j].style.background = "#ccc";
                }
                lists[i].style.display = "block";
                console.log(i);
                links[i].style.background = "red";
            }
        }
        var tmall1 = document.querySelectorAll(".con-list1");
        var tmall2 = document.querySelectorAll(".con-foot-a");
        console.log(tmall1);
        console.log(tmall2);
        for (let i = 0; i < tmall1.length; i++) {
            tmall1[i].onclick = function () {
                for (let j = 0; j < tmall2.length; j++) {
                    tmall2[j].style.display = "none";
                    tmall1[j].style.background = "#f1f1f1"
                    tmall1[j].style.color = "black";
                }
                tmall2[i].style.display = "block";
                tmall1[i].style.background = "#00B262";
                tmall1[i].style.color = "#fff";
            }
        }
        var flag = true;
        setInterval(function () {
            if (flag) {
                tmall2[0].style.display = "block";
                tmall1[0].style.background = "#00B262";
                tmall1[0].style.color = "#fff";
                tmall2[1].style.display = "none";
                tmall1[1].style.background = "#f1f1f1"
                tmall1[1].style.color = "black";
                flag = false;
            } else {
                tmall2[1].style.display = "block";
                tmall1[1].style.background = "#00B262";
                tmall1[1].style.color = "#fff";
                tmall2[0].style.display = "none";
                tmall1[0].style.background = "#f1f1f1"
                tmall1[0].style.color = "black";
                flag = true;
            }
        }, 1500);
    </script>
</body>

</html>
