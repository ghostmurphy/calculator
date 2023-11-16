# calculator
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Калькулятор</title>
    <style>
        .percent{
            display: inline-block
        }
        percent:before{
            content: '%';
            vertical-align: baseline;
        }
    </style>
<body>
    <form mrthod = "post" action = "calculator.js">
        <label for = num1>Число 1:</label>
        <input type = "number" id = "num1" name = "num1" required>

        <label for = num2>Число 2:</label>
        <input type = "number" id = "num2" name = "num2" required>

        <label for = num1>Результат:</label>
        


        <label for = "operator">Операция</label>
        <select id = "operator" name = "operator" required>
            <option value = "+">+</option>
            <option value = "-">-</option>
            <option value = ":">/</option>
            <option value = "*">*</option>
            <option value = "%">%</option>
        </select>
            <input type = "button" value = "Вычислить" onclick = "Function1()">
                                     
        </form>   
        <script type="text/javascript">
            function Function1()
            {
                var num1  = document.getElementById("num1").value;
var num2  = document.getElementById("num2").value;
var operator  = document.getElementById("operator").value;
var result;

switch(operator)
{
   case '+':
    result =  (+num1)+num2;
    break;
   case '-':
    result = num1 - num2;
    break;
   case "*":
    result = num1 * num2;
    break;
   case ':':
    if (num2 == 0) {
        document.write("Ошибка. На ноль делить нельзя");
    } else
    {
        result = num1/num2;
    } 
   case '%':
    result = num1*num2/100;
    break;
   default:
    result = document.write("Введите операцию");
    break;
}

    alert(result);
            }
        
        </script>   
   
</body>
</html>                                             
