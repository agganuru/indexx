# simple-calculator.htm
<!DOCTYPE html>
<html lang="en">
  <head>
      <meta charset="utf-8">
      <meta name="viewport" content="width=device-width,initial-scale=1.0">
      <link rel="stylesheet" href="style..css">
      <title>simple calculator</title>
  </head>
  <body>
      <div class="container">
          <div class="calculator">
              <input type="text"  placeholder="0" id="output-screen">
              <button onclick="clear()">CL</button>
              <button onclick="del()">DEL</button>
              <button onclick="display('%')">%</button>
              <button onclick="display('/')">/</button>
              <button onclick="display('7')">7</button>
              <button onclick="display('8')">8</button>
              <button onclick="display('9')">9</button>
              <button onclick="display('*')">*</button>
              <button onclick="display('4')">4</button>
              <button onclick="display('5')">5</button>
              <button onclick="display('6')">6</button>
              <button onclick="display('-')">-</button>
              <button onclick="display('1')">1</button>
              <button onclick="display('2')">2</button>
              <button onclick="display('3')">3</button>
              <button onclick="display('+')">+</button>
              <button onclick="display('.')">.</button>
              <button onclick="display('0')">0</button>
              <button onclick="calculate()" class="equal">=</butto>
            </div>
      </div>
      <script>
          let outputscreen = document.getElementById("output-screen");
          function display(num){
              outputscreen.value += num;
          }
          function calculate(){
              try{
                  outputscreen.value =eval(outputscreen.value)
              }
              catch(err){
                  alert("invalid")
              }
          }
          function clear(){
              outputscreen.value = "";
         }
         function del(){
             outputscreen.value = outputscreen.value.slice(0,2);
         }
         
      </script>

  </body>
</html> 
