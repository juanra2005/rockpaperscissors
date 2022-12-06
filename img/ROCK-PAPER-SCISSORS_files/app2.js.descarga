const resultText = document.getElementById("start-text");

rock = () => {
    document.getElementById("player-img").src = "img/rock.png";
    document.getElementById("player-img").value = "0";
}

paper = () => {
    document.getElementById("player-img").src = "img/paper.png";
    document.getElementById("player-img").value = "1";
}

scissors = () => {
    document.getElementById("player-img").src = "img/scissors.png";
    document.getElementById("player-img").value = "2";
}


imgramdom = () => {

    let image = Math.floor(Math.random() * 3);
    switch (image) {
        case 0:
            document.getElementById("machine-img").src = "img/rock.png";
            document.getElementById("machine-img").value = "0";
            break;
        case 1:
            document.getElementById("machine-img").src = "img/paper.png";
            document.getElementById("machine-img").value = "1";
            break;
        case 2:
            document.getElementById("machine-img").src = "img/scissors.png";
            document.getElementById("machine-img").value = "2";
            break;
    }
    return;
}

score = () => {

    let selectPlayer, selectMachine;
    selectPlayer = document.getElementById("player-img").value;
    selectMachine = document.getElementById("machine-img").value;


    if (selectPlayer == '0' && selectMachine == '2') {
        scorePlayer();
        resultText.innerHTML = "You win!";
    }
    else if (selectPlayer == '1' && selectMachine == '0') {
        scorePlayer();
        resultText.innerHTML = "You win!";
    }
    else if (selectPlayer == '2' && selectMachine == '1') {
        scorePlayer();
        resultText.innerHTML = "You win!";
    }
    else if (selectMachine == '0' && selectPlayer == '2') {
        scoreMachine();
        resultText.innerHTML = "You lost!";
    }
    else if (selectMachine == '1' && selectPlayer == '0') {
        scoreMachine();
        resultText.innerHTML = "You lost!";
    }
    else if (selectMachine == '2' && selectPlayer == '1') {
        scoreMachine();
        resultText.innerHTML = "You lost!";
    }
    else if (selectPlayer == '0' && selectMachine == '0') {
        resultText.innerHTML = "You have tied!";
    }
    else if (selectPlayer == '1' && selectMachine == '1') {
        resultText.innerHTML = "You have tied!";
    }
    else if (selectPlayer == '2' && selectMachine == '2') {
        resultText.innerHTML = "You have tied!";
    }
    return;
}
let result
scorePlayer = () => {
    result = parseInt(document.getElementById("matchPlayer").innerHTML) + 1;
    document.getElementById("matchPlayer").innerHTML = result;
    return;
}
scoreMachine = () => {
    result = parseInt(document.getElementById("matchMachine").innerHTML) + 1;
    document.getElementById("matchMachine").innerHTML = result;
    return;
}
winner = () => {
    let counter = parseInt(document.getElementById("matchPlayer").innerHTML);
    if (counter == 3) {
        alert("Congratulation you are the winner 👏🏽");
        reset();
        return;
    }
    counter = parseInt(document.getElementById("matchMachine").innerHTML);
    if (counter == 3) {
        alert("You lost against the machine 👎🏽");
        reset();
        return;
    }
}
reset = () => {
    document.getElementById("matchPlayer").innerHTML = "0";
    document.getElementById("matchMachine").innerHTML = "0";
    document.getElementById("player-img").src = "img/signo.png";
    document.getElementById("machine-img").src = "img/signo.png";
    document.getElementById("start-text").innerHTML = "...";
}

play = () => {
    imgramdom();
    score();
    setInterval(winner, 2000);
}