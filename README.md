<template>
<html>

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Alumni Website</title>
    <!-- <link rel="stylesheet" href="css/style.css" />-->
    <!-- CSS only -->

    <header>
        <h1>
            Alumni Website
        </h1>
    </header>
</head>

<body>
    <div>

        <nav>

            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">Alumni Community</a></li>
                <li><a href="#">Contact Us </a></li>
            </ul>
        </nav>
        <div id="slider">

            <ul id="slideWrap">
                <li><img src="../assets/img11.jpg" alt="Alumni Gallery"></li>
                <li> <img src="../assets/img12.jpg" alt="Alumni Gallery"></li>
                <li><img src="../assets/img13.jpg" alt="Alumni Gallery"></li>
                <li><img src="../assets/img14.jpg" alt="Alumni Gallery"></li>
                <li><img src="../assets/img15.jpg" alt="Alumni Gallery"></li>
                

            </ul>
            <a id="prev" href="#">&#8810;</a>
            <a id="next" href="#">&#8811;</a>

        </div>
    </div>

     <footer class="f">
  <p>&copy; 2021 Alumni</p> <br>
  <p><a href="#">Alumni@example.com</a></p>
</footer>
<footer>
    <address>
        Written by <a href="#">Shyam</a>.<br> 
        Visit us at:<br>

        Karve Road, Pune<br>
        Maharashtra
        </address>
      </footer>
<footer>
  <p align="center">
  Some copyright info or perhaps some author
  info for the website.
  </p>
</footer>
</body>

</html>

</template>

<script>

export default{
    name:"indexTwo"
}
var responsiveSlider = function () {

    var slider = document.getElementById("slider");
    var sliderWidth = slider.offsetWidth;
    var slideList = document.getElementById("slideWrap");
    var count = 1;
    var items = slideList.querySelectorAll("li").length;
    var prev = document.getElementById("prev");
    var next = document.getElementById("next");

    window.addEventListener('resize', function () {
        sliderWidth = slider.offsetWidth;
    });

    var prevSlide = function () {
        if (count > 1) {
            count = count - 2;
            slideList.style.left = "-" + count * sliderWidth + "px";
            count++;
        } else if (count == 1) {
            count = items - 1;
            slideList.style.left = "-" + count * sliderWidth + "px";
            count++;
        }
    };

    var nextSlide = function () {
        if (count < items) {
            slideList.style.left = "-" + count * sliderWidth + "px";
            count++;
        } else if (count == items) {
            slideList.style.left = "0px";
            count = 1;
        }
    };

    next.addEventListener("click", function () {
        nextSlide();
    });

    prev.addEventListener("click", function () {
        prevSlide();
    });

    setInterval(function () {
        nextSlide()
    }, 5000);

};

window.onload = function () {
    responsiveSlider();
}


</script>

        

    
        





<style>
ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    overflow: hidden;
    background-color: #dddddd;

}

li {
    float: left;
}

li a {
    display: block;
    text-align: center;
    color: white;
    padding: 14px 16px;
    text-decoration: none;
}

li a:hover {
    background-color: #111;
}

body {
    margin: 10%;
    margin-left: 20%;
}

#slider {
    position: relative;
    width: 500px;
    height: 265px;

    overflow: hidden;
    box-shadow: 0 0 30px rgba(0, 0, 0, 0.3);
}

#slider ul {
    position: relative;
    list-style: none;
    height: 100%;
    width: 10000%;
    padding: 0;
    margin: 0;
    transition: all 750ms ease;
    left: 0;
}

#slider ul li {
    position: relative;
    height: 100%;

    float: left;
}

#slider ul li img {
    width: 2000px;
    height: 1000px;
}

#slider #prev,
#slider #next {
    width: 50px;
    line-height: 50px;
    border-radius: 50%;
    font-size: 2rem;
    text-shadow: 0 0 20px rgba(0, 0, 0, 0.6);
    text-align: center;
    color: white;
    text-decoration: none;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    transition: all 150ms ease;
}

#slider #prev:hover,
#slider #next:hover {
    background-color: rgba(0, 0, 0, 0.5);
    text-shadow: 0;
}

#slider #prev {
    left: 10px;
}

#slider #next {
    right: 10px;
}
</style>-->
<style>
*{
    margin:0;
    padding:0;
}

body{
    width:100%;
    height:100vh;
    

}
ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    overflow: hidden;
    width: 100%;

}

li {
    float: left;

}

li a {
    display: block;
    padding: 8px;
    background-color: #dddddd;
    width: 100%;
}
#slider {
    position: relative;
    width: 1600px;
    height: 600px;

    overflow: hidden;
    box-shadow: 0 0 30px rgba(0, 0, 0, 0.3);
}

#slider ul {
    position: relative;
    list-style: none;
    height: 100%;
    width: 10000%;
    padding: 0;
    margin: 0;
    transition: all 750ms ease;
    left: 0;
}

#slider ul li {
    position: relative;
    height: 100%;

    float: left;
}

#slider ul li img {
    width: 100%;
    height: 1000px;
}

#slider #prev,
#slider #next {
    width: 50px;
    line-height: 50px;
    border-radius: 50%;
    font-size: 2rem;
    text-shadow: 0 0 20px rgba(0, 0, 0, 0.6);
    text-align: center;
    color: white;
    text-decoration: none;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    transition: all 150ms ease;
}

#slider #prev:hover,
#slider #next:hover {
    background-color: rgba(0, 0, 0, 0.5);
    text-shadow: 0;
}

#slider #prev {
    left: 10px;
}

#slider #next {
    right: 10px;
}
.split {
  height: auto;
  width: 50%;
  position: fixed;
  z-index: 1;
  top: 0;
  overflow-x: hidden;
  padding-top: 20px;
}

.left {
  left: 0;
  background-color: gray;
}

.right {
  right: 0;
  background-color:gainsboro;
}

.centered {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
}


</style>


