function initDate(){
    const now = new Date();
    var seconds = now.getSeconds();
    secondDeg = ((seconds / 60) * 360) + 90;
    // console.log(secondDeg);
    
    var minutes = now.getMinutes();
    minuteDeg = ((minutes / 60) * 360) + 90;
    // console.log(minuteDeg);
    var hours = now.getHours();
    hourDeg = ((hours / 12) * 360) + 90 + (minutes / 60);
    // console.log(hourDeg);
  }
  function updateDate(){
    secondDeg += ((1 / 60) * 360);  //秒針每秒跑的度數
    minuteDeg += ((1 / 60 /60) * 360); //一分=360秒 分針每秒跑的度數
    hourDeg += ((1 / 60/ 60/ 12) *360 ); //一小時= 60x60x12= 4320秒
    secondHand.style.transform = `rotate(${secondDeg}deg)`;
    minuteHand.style.transform = `rotate(${minuteDeg}deg)`;
    hourHand.style.transform = `rotate(${hourDeg}deg)`;
  }
