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

<style>
div{
    color:pink; 
    text-shadow: 0px 0px 70px;
}
</style>

<!-- slide -->
<div id=1 ></div>

:smile:


<!-- slide -->
<div id=2>今天是不是又是努力奋斗的一天呢？</div>




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
</script>
