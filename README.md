var inputOne = "";
var inputTwo = "";
var firstInput = true;
var operation = "";
var calcText = "";

//Handle 1 button press
onEvent("oneButton", "click", function(event) {
  console.log("oneButton clicked!");
  if (firstInput == true) {
    inputOne = inputOne + "1";
    setText("calculatorScreen",  inputOne);
  } else {
    inputTwo = inputTwo + "1";
    setText("calculatorScreen", calcText + inputTwo);
  }
});

//Handle 2 button press
onEvent("twoButton", "click", function(event) {
  console.log("oneButton clicked!");
  if (firstInput == true) {
    inputOne = inputOne + "2";
    setText("calculatorScreen", inputOne);
  } else {
    inputTwo = inputTwo + "2";
    setText("calculatorScreen", calcText + inputTwo);
  }
});
onEvent("threeButton", "click", function(event) {
  console.log("oneButton clicked!");
  if (firstInput == true) {
    inputOne = inputOne + "3";
    setText("calculatorScreen", inputOne);
  } else {
    inputTwo = inputTwo + "3";
    setText("calculatorScreen", calcText + inputTwo);
  }
});
onEvent("fourButton", "click", function(event) {
  console.log("oneButton clicked!");
  if (firstInput == true) {
    inputOne = inputOne + "4";
    setText("calculatorScreen", inputOne);
  } else {
    inputTwo = inputTwo + "4";
    setText("calculatorScreen", calcText + inputTwo);
  }
});
onEvent("fiveButton", "click", function(event) {
  console.log("oneButton clicked!");
  if (firstInput == true) {
    inputOne = inputOne + "5";
    setText("calculatorScreen", inputOne);
  } else {
    inputTwo = inputTwo + "5";
    setText("calculatorScreen", calcText + inputTwo);
  }
});
onEvent("sixButton", "click", function(event) {
  console.log("oneButton clicked!");
  if (firstInput == true) {
    inputOne = inputOne + "6";
    setText("calculatorScreen", inputOne);
  } else {
    inputTwo = inputTwo + "6";
    setText("calculatorScreen", calcText + inputTwo);
  }
});
onEvent("sevenButton", "click", function(event) {
  console.log("oneButton clicked!");
  if (firstInput == true) {
    inputOne = inputOne + "7";
    setText("calculatorScreen", inputOne);
  } else {
    inputTwo = inputTwo + "7";
    setText("calculatorScreen", calcText + inputTwo);
  }
});
onEvent("eightButton", "click", function(event) {
  console.log("oneButton clicked!");
  if (firstInput == true) {
    inputOne = inputOne + "8";
    setText("calculatorScreen", inputOne);
  } else {
    inputTwo = inputTwo + "8";
    setText("calculatorScreen", calcText + inputTwo);
  }
});
onEvent("nineButton", "click", function(event) {
  console.log("oneButton clicked!");
  if (firstInput == true) {
    inputOne = inputOne + "9";
    setText("calculatorScreen", inputOne);
  } else {
    inputTwo = inputTwo + "9";
    setText("calculatorScreen", calcText + inputTwo);
  }
});
onEvent("zeroButton", "click", function(event) {
  console.log("oneButton clicked!");
  if (firstInput == true) {
    inputOne = inputOne + "0";
    setText("calculatorScreen", inputOne);
  } else {
    inputTwo = inputTwo + "0";
    setText("calculatorScreen", calcText + inputTwo);
  }
});

/*The plus button is clicked, set the operation to addition
toggle the input from inputOne to inputTwo
*/
onEvent("plusButton", "click", function(event) {
  console.log("plusButton clicked!");
  firstInput = false;
  operation = "add"
  calcText = inputOne + " + ";
  
  setText("calculatorScreen", calcText);
});
onEvent("minusButton", "click", function(event) {
  console.log("minusButton clicked!");
  firstInput = false;
  operation = "subtract";
  calcText = inputOne + " - ";
  setText("calculatorScreen", calcText);
});
onEvent("divideButton", "click", function(event) {
  console.log("divideButton clicked!");
  firstInput = false;
  operation = "divide";
  calcText = inputOne + " / ";
  setText("calculatorScreen", calcText);
});
onEvent("multiplyButton", "click", function(event) {
  console.log("multiplyButton clicked!");
  firstInput = false;
  operation = "multiply";
  calcText = inputOne + " * ";
  setText("calculatorScreen", calcText);
});
/*
After values have been set, calculate the output
*/
onEvent("equalButton", "click", function(event) {
  console.log("equalButton clicked!");
  var value1 = parseInt(inputOne);
  var value2 = parseInt(inputTwo);
  var result;
  if(operation === "add") {
      result = value1 + value2;
  }
  
  if(operation === "subtract") 
      result = value1 - value2;
      
  if(operation === "divide") 
      result = value1 / value2;
  if (value2 == 0) {
    result = "Error";
    
  }
    ;

      
  if(operation === "multiply") 
      result = value1 * value2;

  //update calculator text
  var finalCalcText = getText("calculatorScreen") + " = " + result;
  setText("calculatorScreen", finalCalcText);
  }
);


//Clear screen and reset values
onEvent("button18", "click", function(event) {
  console.log("button18 clicked!");
  setText("calculatorScreen", "...");
  inputOne = "";
  inputTwo = "";
  firstInput = true;
  
});
