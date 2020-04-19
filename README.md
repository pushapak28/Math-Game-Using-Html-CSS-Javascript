# Math-Game-Using-Html-CSS-Javascript
Simple using of html Css JavaScript easy code written basic mathematical game MCQs type. 

//html code 

<!DOCTYPE html>
<html lang="">

<head>
    <title>Maths Game</title>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0 user-scalable=yes">
    <link rel="stylesheet" href="styling.css">
</head>

<body>
    <div id="container">
        <div id="score"> Score: 
            <span id="scorevalue">0</span>
        </div>
        <div id="correct"> Correct </div>
        <div id="wrong"> Try again </div>
        <div id="question"> </div>
        <div id="instruction">
            Click on the correct answer </div>
        <div id="choices">
            <div id="box1" class="box"></div>
            <div id="box2" class="box"></div>
            <div id="box3" class="box"></div>
            <div id="box4" class="box"></div>
        </div>
        <div id="startreset"> Start Game </div>
        <div id="timeremaining"> Time remaining: <span id="timeremainingvalue">60</span> sec </div>
        <div id="gameOver"> </div>
    </div>
    <script src="javascript.js">
  
</script>
</body>

</html>

//basic CSS code

html {
    height: 100%;
    background-image: url(back%202.jpg);
    /*background: radial-gradient(circle, #fff, #ccc);
    background: -webkit-radial-gradient(circle, #fff, #ccc);
    background: -o-radial-gradient(circle, #fff, #ccc);
    background: -moz-radial-gradient(circle, #fff, #ccc);*/
}



#container {
    height: 400px;
    width: 550px;
    background-color:#77BBD0;  
    margin: 100px auto;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0px 4px 0px 0px #009de4;
    -moz-box-shadow: 0px 4px 0px 0px #009de4;
    -webkit-box-shadow: 0px 4px 0px 0px #009de4;
    /*        box-shadow: [horizontal offset] [vertical offset] [blur radius] [optional spread radius] [color]*/
    position: relative;
}

#score {
    background-color: #F1FF92;
    color: #888E5F;
    padding: 11px;
    position: absolute;
    left: 500px;
    box-shadow: 0px 4px 0px #9da853;
    -moz-box-shadow: 0px 4px 0px #9da853;
    -webkit-box-shadow: 0px 4px 0px #9da853;
}

#correct {
    position: absolute;
    left: 260px;
    background-color: #42e252;
    color: white;
    padding: 11px;
    display: none;
}

#wrong {
    position: absolute;
    left: 250px;
    background-color: #de401a;
    color: white;
    padding: 11px;
    display: none;
}

#question {
    width: 450px;
    height: 150px;
    margin: 50px auto 10px auto;
    background-color: #9DA0EA;
    box-shadow: 0px 4px #535aa8;
    -moz-box-shadow: 0px 4px #535aa8;
    -webkit-box-shadow: 0px 4px #535aa8;
    font-size: 100px;
    text-align: center;
    font-family: cursive, sans-serif;
    color: black;
}

#instruction {
    width: 450px;
    height: 50px;
    background-color: #B481D9;
    margin: 10px auto;
    text-align: center;
    line-height: 45px;
    box-shadow: 0px 4px #8153a8;
    -moz-box-shadow: 0px 4px #8153a8;
    -webkit-box-shadow: 0px 4px #8153a8;
}

#choices {
    width: 450px;
    height: 100px;
    margin: 5px auto;
}

.box {
    width: 85px;
    height: 85px;
    background-color: white;
    float: left;
    margin-right: 36px;
    border-radius: 3px;
    cursor: pointer;
    box-shadow: 0px 4px rgba(0, 0, 0, 0.2);
    -moz-box-shadow: 0px 4px rgba(0, 0, 0, 0.2);
    -webkit-box-shadow: 0px 4px rgba(0, 0, 0, 0.2);
    text-align: center;
    line-height: 80px;
    position: relative;
    transition: all 0.2s;
    -webkit-transition: all 0.2s;
    -moz-transition: all 0.2s;
    -o-transition: all 0.2s;
    -ms-transition: all 0.2s;
}

.box:hover,
#startreset:hover {
    /*    background-color: #9C89F6;*/
    /*    color: white;*/
    /*    box-shadow: 0px 4px #6b54d3;*/
    /*    -moz-box-shadow: 0px 4px #6b54d3;*/
    /*    -webkit-box-shadow: 0px 4px #6b54d3;*/
}

.box:active,
#startreset:active {
    background-color: #9C89F6;
    color: white;
    box-shadow: 0px 0px #6b54d3;
    -moz-box-shadow: 0px 0px #6b54d3;
    -webkit-box-shadow: 0px 0px #6b54d3;
    top: 4px;
}

#box4 {
    margin-right: 0;
}

#startreset {
    width: 78px;
    padding: 10px;
    background-color: rgba(255, 255, 255, 0.5);
    margin: 0 auto;
    border-radius: 3px;
    cursor: pointer;
    box-shadow: 0px 4px rgba(0, 0, 0, 0.2);
    -moz-box-shadow: 0px 4px rgba(0, 0, 0, 0.2);
    -webkit-box-shadow: 0px 4px rgba(0, 0, 0, 0.2);
    text-align: center;
    position: relative;
    transition: all 0.2s;
    -webkit-transition: all 0.2s;
    -moz-transition: all 0.2s;
    -o-transition: all 0.2s;
    -ms-transition: all 0.2s;
}

#timeremaining {
    width: 152px;
    padding: 10px;
    position: absolute;
    top: 395px;
    left: 400px;
    background-color: rgba(181, 235, 36, 0.8);
    border-radius: 3px;
    box-shadow: 0px 4px rgba(0, 0, 0, 0.2);
    -moz-box-shadow: 0px 4px rgba(0, 0, 0, 0.2);
    -webkit-box-shadow: 0px 4px rgba(0, 0, 0, 0.2);
    /* visibility: hidden;*/
    display: none;
}

#gameover {
    height: 200px;
    width: 500px;
    background: linear-gradient(#F3CA6B, #F3706C);
    background: -webkit-linear-gradient(#F3CA6B, #F3706C);
    background: -o-linear-gradient(#F3CA6B, #F3706C);
    background: -moz-linear-gradient(#F3CA6B, #F3706C);
    color: white;
    font-size: 2.5em;
    text-align: center;
    text-transform: uppercase;
    position: absolute;
    top: 100px;
    left: 45px;
    z-index: 2;
    display: none;
}

//javacript
  //javascript.js 
var playing = false;
var score;
var action;
var timeremaining;
var correctAnswer;

//if we click on the start/reset 
document.getElementById("startreset").onclick = function () {
    //if we are playing 
    if (playing == true) {
        location.reload();
        //reload page              
    } else {
        //if we are not playing                  //change mode to playing                  
        playing = true; //set score to 0                  
        score = 0;
        document.getElementById("scorevalue").innerHTML = score; //show countdown box                   
        show("timeremaining");
        timeremaining = 60;
        document.getElementById("timeremainingvalue").innerHTML = timeremaining; //hide game over box               
        hide("gameOver"); //change button to reset         
        document.getElementById("startreset").innerHTML = "Reset Game";
        //start countdown                  
        startCountdown(); //generate a new Q&A                  
        generateQA();
    }
}

//Clicking on an answer box 

for (i = 1; i < 5; i++) {
    document.getElementById("box" + i).onclick = function () {
        //check if we are playing          
        if (playing == true) {
            //yes         
            if (this.innerHTML == correctAnswer) { //correct answer                
                //increase score by 1          
                score++;
                document.getElementById("scorevalue").innerHTML = score;

                //hide wrong box and show correct box           
                hide("wrong");
                show("correct");
                setTimeout(function () {
                    hide("correct");
                }, 1000);

                //Generate new Q&A                          
                generateQA();
            } else {
                //wrong answer             
                hide("correct");
                show("wrong");
                setTimeout(function () {
                    hide("wrong");
                }, 1000);
            }
        }
    }
}
//if we click on answer box    
//if we are playing       
//correct?           
//yes               
//increase score                 //show correct box for 1sec                 //generate new Q&A                         //no        
//show try again box for 1sec 


//functions 

//start counter 

function startCountdown() {
    action = setInterval(function () {
        timeremaining -= 1;
        document.getElementById("timeremainingvalue").innerHTML = timeremaining;
        if (timeremaining == 0) {
            // game over             
            stopCountdown();
            show("gameOver");
            document.getElementById("gameOver").innerHTML = "<p>Game over!</p><p>Your score is " + score + ".</p>";
            hide("timeremaining");
            hide("correct");
            hide("wrong");
            playing = false;
            document.getElementById("startreset").innerHTML = "Start Game";
        }
    }, 1000);
}

//stop counter 

function stopCountdown() {
    clearInterval(action);
}

//hide an element 

function hide(Id) {
    document.getElementById(Id).style.display = "none";
}

//show an element 

function show(Id) {
    document.getElementById(Id).style.display = "block";
}

//generate question and multiple answers 

function generateQA() {
    var x = 1 + Math.round(9 * Math.random());
    var y = 1 + Math.round(9 * Math.random());
    correctAnswer = x * y;
    document.getElementById("question").innerHTML = x + "x" + y;
    var correctPosition = 1 + Math.round(3 * Math.random());
    document.getElementById("box" + correctPosition).innerHTML = correctAnswer;
    //fill one box with the correct answer       
    //fill other boxes with wrong answers        
    var answers = [correctAnswer];
    for (i = 1; i < 5; i++) {
        if (i != correctPosition) {
            var wrongAnswer;
            do {
                wrongAnswer = (1 + Math.round(9 * Math.random())) * (1 + Math.round(9 * Math.random()));
                //a wrong answer            
            }
            while (answers.indexOf(wrongAnswer) > -1)
            document.getElementById("box" + i).innerHTML = wrongAnswer;
            answers.push(wrongAnswer);
        }
    }
}
