---
presentation:
    # presentation 主题
    # === 可选的主题 ===
    # "beige.css"
    # "black.css"
    # "blood.css"
    # "league.css"
    # "moon.css"
    # "night.css"
    # "serif.css"
    # "simple.css"
    # "sky.css"
    # "solarized.css"
    # "white.css"
    # "none.css"
    theme: blood.css

    width: 800
    height: 600

    margin: 0.1

    minScale: 0.2
    maxScale: 1.5
---

<head>
    <title></title>
</head>

<style>
div{
    color:pink; 
    text-shadow: 0px 0px 70px;
}

}
</style>

<!-- slide -->
<div id=1></div>

:smile:


<!-- slide -->
<div id=2>今天是不是<br>也是努力奋斗的一天呢？</div>

<!-- slide -->
<div id=3>还记得是什么时候开始<br>你也过上了“考研狗”的生活吗？<br>一日复一日的拼搏</div>

<div>自习室、图书馆早已成为你熟悉的“狗窝”<br>一坐就是一天<br>只有你能够耐住这样的寂寞</div>

<!-- slide -->
<div id=4>还记得那天，是
<form name=date>
    <input type="text" name=year id=year style="width:100px;font-size:20px"></input>年
    <input type="text" name=month id=month style="width:70px;font-size:20px"></input>月
    <input type="text" name=day id=day style="width:70px;font-size:20px"></input>日
</form><br>
<button onclick="dateCommit()" style="font-size:20px">确定</button>
</div>

<br>
<div id=5 style=display:none>记得那一天<br><br>你下定决心<br><br>决意要考研</div>

<!-- slide -->
<div>转眼间，已经过去了<br>
<span id=6></span><span id=7></span><span id=8></span>
</div>

<!-- slide -->
<div>
在这<span id=9></span> 天里<br>
你一直努力拼搏<br>

</div>

<!-- slide -->
<div>时间过得真是快呀 <br>

:clock1:

<span>还有</span><span id=10></span> 天就要考试啦

</div>
<!-- slide -->
<div>在剩下的时间里
<br>
希望你能够沉住气继续前行
<br>
稳住心态，你一定会上岸！
<br>
你一定能成功！
</div>

:sunny:

<script>
    var d = new Date();
    var e = document.getElementById("1");
    var str = new String();
    if (d.getHours() >= 18)
        str += "晚 上 ";
    else
        str += "早 上 ";
    str += "好 呀";

    e.innerHTML = str;
    e = document.getElementById("10");
    var examDate = new Date(2021, 11, 25);
    e.innerHTML = examDate.getDate() - d.getDate();
</script>
<script>
    function dateCommit()
    {
        var year = date.year.value;
        var month = date.month.value - 1;
        var day = date.day.value;
        if (day == "")
            day = 1;
        if (year >= 20 && year <= 21)
            year += 2000;

        var e = document.getElementById("5");
		e.style.display='block';
        e = document.getElementById("4");
		e.style.display='none';

        var d = new Date();
        var thatDay = new Date(year, month, day);
        console.log(thatDay);
        console.log(d);
        var days = parseInt((d - thatDay) / 1000 / 60 / 60 / 24);


        e = document.getElementById("6");
        if (parseInt(days / 365) > 0)
            e.innerHTML = parseInt(days / 365) + '年';

        e = document.getElementById("7");
        var ddd;
        if (month < d.getMonth())
            ddd = d.getMonth() - month;
        else
            ddd = d.getMonth() + 12 - month;

        if (day > d.getDate())
            ddd = ddd - 1;

        if (ddd % 12 > 0)
            e.innerHTML = ddd % 12 + '个月';

        e = document.getElementById("8");
        if (d.getDate() > day)
            e.innerHTML = d.getDate() - day + '天';
        if (d.getDate() < day)
            e.innerHTML = d.getDate() + 30 - day + '天';

        
        e = document.getElementById("9");
        e.innerHTML = parseInt(days);

    }

</script>

<!-- 

2020 11 5
2021 2 3

 -->
