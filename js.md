# 1.	Đặc tính
-	Thay đổi , chỉnh sửa html attribute , css,…
-	Xử lý các event
-	Sử dụng thẻ <script></script> , external js sử dụng file.js
# 2.	Nội dung
-	Display data bằng cách: innerHTML(trong html element), document.write(),window.alert(), console.log().
-	Access an HTML element using document.getElementById() method.
-	javaScript code blocks: để nhóm lại các khối code blocks, trong dấu ngoặc nhọn, để chúng chạy cùng nhau.
-	Khai báo biến bằng var: global scope; let: block scope; const: giá trị mặc định.
-	Code after double slashes // or between /* */ is treated as a comment.
-	Javascript phân biệt chữ hoa với chữ thường. = là gán, == so sánh giá trị ko phân biệt loại giữ liệu, === bằng mọi thứ.
-	các loại data types: number, string, boolean, object, function.
6 types of object: object,Date,array, string, number, boolean. Underfined : biến không có giá trị , hoặc giá trị là underfined; null là vô giá trị .
# 3.	object
-	bao gồm method, property: value.
-	this keyword in function refer to the “owner” of the function; đại diện  cho object; in an event this refers to the element that reveived the event.
```
document.getElementById('demo').innerHTML = "hello \
DOlly!";
```
dùng \ khi muốn xuống dòng trong lúc viết string.
# 4.	Method in js
-	indexOf() thứ tự của phần tử tính từ đầu. lastIndexOf() tương tự nhưng từ cuối.
-	Search() tìm kiếm vị trí phần tử. 
```
var pos = str.search("locate");
```
-slice() lấy một đoạn string từ vị trí bao nhiêu đến bao nhiêu
```
var str = "Apple, Banana, Kiwi";
var res = str.slice(7, 13);
```
- substring() tương tự nhưng không chấp nhận số âm.
- replace() đổi vị trí. nhưng chỉ đổi vị trí của CỤM TỪ ĐẦU TIÊN. và cũng nhạy cảm về loại chữ hoa hoặc thường => khắc phục sử dụng `/..../i` nếu muốn thay toàn bộ sử dụng thêm (`/.../g`). insensitive.
```
str = "Please visit Microsoft!";
var n = str.replace("Microsoft", "W3Schools");
``` 
- để convert to upper and lower case thì
```
var text1 = "Hello World!";    
var text2 = text1.toUpperCase();
```
```
var text1 = "Hello World!";    
var text2 = text1.toLowerCase();
```
- dùng concat() để nối các string , array, ... với nhau.
```
var text1 = "Hello";
var text2 = "World";
var text3 = text1.concat(" ", text2);
var text1 = "Hello";
var text2 = "World";
var text3 = text1.concat(" ", text2);
```
- trim() để xóa khoảng trắng ở 2 bên
```
var str = "       Hello World!        ";
alert(str.trim());

```
- The charAt() Method để lấy ra kí tự bằng vị trí
```
var str = "HELLO WORLD";
str.charAt(0);  return "H"
```
- còn charCodeAt() là mã hóa nó.
- Converting a String to an Array, chuyển string sang array.
```
var txt = "a,b,c,d,e";   // String
txt.split(",");          // Split on commas
txt.split(" ");          // Split on spaces
txt.split("|");          // Split on pipe
```
- NAN not a number là 1 loại số nhưng ko là số gì. infinity or -infinity là giá trị vô cực.
- toString() đổi number ra string.
- The toFixed() Method xác định số chữ số cố định sau dấu phảy. thường dùng để viết money.
```
var x = 9.656;
x.toFixed(0);           // returns 10
x.toFixed(2);           // returns 9.66
x.toFixed(4);           // returns 9.6560
x.toFixed(6);           // returns 9.656000
```
- The toPrecision() Method  dùng để làm tròn.
```
var x = 9.656;
x.toPrecision();        // returns 9.656
x.toPrecision(2);       // returns 9.7
x.toPrecision(4);       // returns 9.656
x.toPrecision(6);       // returns 9.65600
```
- Converting Variables to Numbers có 3 cách:
     +) Number() method
     +) parseInt() method
     +) parseFloat() method

// array method.

- Converting Arrays to Strings sử dụng join();
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.join(" * ");
```
- Splicing an Array nối , thêm vào bên trong array. nghĩa là ở chuỗi thứ 2 loại bỏ 0 chuỗi thêm  "Lemon", "Kiwi" vào.
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(2, 0, "Lemon", "Kiwi");
```
- Slicing an Array : cắt 1 đoạn trong array ra làm array mới. từ sau chuỗi số 1 tạo thành array mới.
```
var fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
var citrus = fruits.slice(1);
```
- map(),forEach() : tạo mảng mới cho các phần tử.
- filter() dùng để lọc phần tử.
- every() mọi phần tử thỏa mãn trả về true
- some() một phần tử thỏa mãn cũng trả về true
- indexOf() trả về vị trí của phần tử trong Array.
```
var fruits = ["Apple", "Orange", "Apple", "Mango"];
var a = fruits.lastIndexOf("Apple");
```
- Array.find() trả về phần tử đầu tiên thỏa mãn.
- findIndex() trả về vị trí phần tử đầu tiên thỏa mãn.

// number method.

- Math.round() làm tròn.
- Math.abs() giá trị tuyệt đối
- Math.ceil() làm tròn lên.
- Math.float() làm tròn xuống.
- Math.random().
```
Math.floor(Math.random()* 10);
```
# 5. statement condition,loop
- if() else if() {} else{}.
- switch biểu diễn kết quả khác nhau với điều kiện khác nhau.
```
<script>
var day;
switch (new Date().getDay()) {
  case 0:
    day = "Sunday";
    break;
  case 1:
    day = "Monday";
    break;
  case 2:
    day = "Tuesday";
    break;
  case 3:
    day = "Wednesday";
    break;
  case 4:
    day = "Thursday";
    break;
  case 5:
    day = "Friday";
    break;
  case  6:
    day = "Saturday";
}
document.getElementById("demo").innerHTML = "Today is " + day;
</script>
```
```
switch (new Date().getDay()) {
  case 4:
  case 5:
    text = "Soon it is Weekend";
    break;
  case 0:
  case 6:
    text = "It is Weekend";
    break;
  default:
    text = "Looking forward to the Weekend";
}
```
- loop for, while: 
- for in : trong object, for of trong array
- sự khác biệt là vòng lặp for được sử dụng khi số lần lặp được biết đến còn while thì chưa .
- js break , nếu nó thỏa mãn điều kiện thì dừng.
```
for (i = 0; i < 10; i++) {
  if (i === 3) { break; }
  text += "The number is " + i + "<br>";
}
```
- js continue , nếu đúng điều kiện bỏ qua nó vẫn tiếp tục.
```
for (i = 0; i < 10; i++) {
  if (i === 3) { continue; }
  text += "The number is " + i + "<br>";
}
```    
- dùng try catch để bắt lỗi:
```
<script>
try {
  adddlert("Welcome guest!");
}
catch(err) {
  document.getElementById("demo").innerHTML = err.message;
}
</script>
```
- dùng khi với vai trò như HTML validation 
```
<script>
function myFunction() {
  var message, x;
  message = document.getElementById("p01");
  message.innerHTML = "";
  x = document.getElementById("demo").value;
  try {
    if(x == "") throw "empty";
    if(isNaN(x)) throw "not a number";
    x = Number(x);
    if(x < 5) throw "too low";
    if(x > 10) throw "too high";
  }
  catch(err) {
    message.innerHTML = "Input is " + err;
  }
}
</script>
```

# 





```

```