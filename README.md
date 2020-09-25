# calculator

<br><br>
계산기를 웹사이트에 구현하면서 자료구조에 대해 진지하게 생각

<h>
 <br>
~~~
 <br>
  사용언어 : HTML, CSS, JavaScript
 <br>
~~~

~~~html
<!DOCTYPE html>

<html lang="en" dir="ltr">

  <head>

    <meta charset="utf-8">

    <link rel="stylesheet" href="./calcul.css">

    <title>calculating machine</title>

    <script type="text/javascript" src="./index.js"></script>

  </head>

  <body>

    <table border=0 height=500 width=400 align="center">

    <form>

    <tr>

      <td colspan= 4 bgcolor="ffdfdc" align="right" height="70" />

      <input id="display" type="text" />

    </tr>

    <tr>

      <td colspan= 4 bgcolor="#ffcbc9" align="left"  height="60"> &emsp;&emsp;result&emsp;:<input id="result" type="text"  />

      </td>

    </tr>

    <tr>

      <td>

        <input type="reset" name="reset" value="AC" class="button3" />

      </td>

      <td>

        <input type="button" name="plus_min" value="+/-" class="button3" />

      </td>

      <td>

        <input type="button" onclick="addOutput('%')" value="%" class="button3" />

      </td>

      <td>

        <input type="button" onclick="addOutput('/')" value="/" class="button3" />

      </td>

    </tr>

    <tr>

      <td>

        <input type="button" onclick="addOutput('7')" value="7" class="button"/>

      </td>

      <td>

        <input type="button" onclick="addOutput('8')" value="8" class="button"/>

      </td>

      <td>

        <input type="button" onclick="addOutput('9')" value="9" class="button"/>

      </td>

      <td>

        <input type="button" onclick="addOutput('*')" value="*"class="button3" />

      </td>

    </tr>

    <tr>

        <td>

          <input type="button" onclick="addOutput('4')" value="4" class="button"/>

        </td>

        <td>

          <input type="button" onclick="addOutput('5')" value="5" class="button"/>

        </td>

        <td>

          <input type="button" onclick="addOutput('6')" value="6" class="button"/>

        </td>

        <td>

          <input type="button" onclick="addOutput('-')" value="-" class="button3" />

        </td>

      </tr>

      <tr>

          <td><input type="button" onclick="addOutput('1')" value="1" class="button"/>

          </td>

          <td>

            <input type="button" onclick="addOutput('2')" value="2" class="button"/>

          </td>

          <td>

            <input type="button" onclick="addOutput('3')" value="3" class="button" />

          </td>

          <td>

            <input type="button" onclick="addOutput('+')" value="+" class="button3" />

          </td>

        </tr>

        <tr>

            <td colspan=2>

              <input type="button" onclick="addOutput('0')" value="0" class="button2"/>

            </td>

            <td>

              <input type="button" onclick="addOutput('.')" value="." class="button" />

            </td>

            <td>

              <input type="button" onclick="calculate()" value="=" class="button3" />

            </td>

          </tr>

    </form>

        </table>

  </body>

</html>

~~~
~~~javascript
function addOutput(num) {
  var display = document.getElementById("display");
  display.value = display.value + num;
}

function calculate() {
  var display = document.getElementById("display");
  var result = eval(display.value);
  var displayResult = document.getElementById("result");
  displayResult.value = result;
}

function reset() {
  var display = document.getElementById("display");
  display.value = "";
  var displayResult = document.getElementById("result");
  displayResult.value = "";
}

function del() {
  var display = documnet.getElementById("display");
  display.value = display.value.substring(0, display.value.length - 1);
}

~~~
~~~css
tr{
text-align: center;

}
.button{
border:1x solid #ff0080;    /*---테두리 정의---*/
background-Color:#ffe6f2;   /*--백그라운드 정의---*/
font:30px 굴림;      /*--폰트 정의---*/
font-weight:bold;   /*--폰트 굵기---*/
color:#ff0080;    /*--폰트 색깔---*/
width:100px;height:100px;  /*--버튼 크기---*/
}

.button2{
  border:1x solid #ff0080;
  background-Color:#ffe6f2;
  font:30px 굴림;
  font-weight:bold;
  color:#ff0080;
  width:210px;height:100px;
}

.button3{
  border:1x solid #ff0080;
  background-Color:#cd919e;
  font:30px 굴림;
  font-weight:bold;
  color:#ff0080;
  width:100px;height:100px;
}

#display,
#result {
  width: 400px;
  height: 50px;
  font-size: 60px;
  font-weight: bold;
  text-align: right;
  padding-right: 8px;
  color : ffdfdc;
}~~~
