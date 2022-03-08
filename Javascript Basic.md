# Javascript cơ bản

## #1 - Giới thiệu về Javascript

-   Javascript là một ngôn ngữ lập trình được phát hành vào năm 1995 và có tên là **mocha**, sau đó được đổi tên là LiveScript và cuối cùng là đổi tên thành **Javascript**
-   Trước kia Javascript chỉ có thể lập trình phía Front-End (Xử lý tương tác với người dùng, tạo hiệu ứng,...). Tuy nhiên, ngày nay Javascript còn có thể lập trình cả Front-End, Back-End hay thậm chí là cả Mobile hoặc Desktop App.

## #2 - Làm sao để thực thi code JS?

-   Cách 1: Nhúng JS vào file HTML và chạy trên trình duyệt
-   Cách 2: Chạy với môi trường NodeJS

## #3 - Biến và Kiểu dữ liệu trong Javascript

#### Tìm hiểu về biến:

\- **Biến** là ô nhớ dùng để lưu trữ giá trị. Mỗi ô nhớ sẽ có 1 địa chỉ riêng (Nó sẽ liên quan đến kiến thức kiểu dữ liệu nguyên thủy và kiểu dữ liệu tham chiếu).
\- **Cú pháp khai báo biến:**

```js
// Cách 1:
var courseName = 'Javascript Basic';

// Cách 2:
let courseName = 'Javascript Basic';
```

\- **Cách đặt tên biến:**

-   Nên đặt tên biến bằng tiếng anh và biến đó chứa giá trị gì.
-   Tên biến phải là các chữ không dấu viết hoa hoặc viết thường, các chữ số từ 0-9 và dấu gạch dưới () và kí hiệu $.
-   Tên biến phải bắt đầu bằng chữ hoặc dấu gạch dưới hoặc $
-   Với những giá trị trả về true hoặc false thì nên đặt prefix is/has hoặc tên biến có ý nghĩa nhận giá trị true hoặc false.
-   Với dạng danh sách thì thêm suffix List: productList, courseList,...

#### Các kiểu dữ liệu trong JS

-   Boolean
-   Null
-   Undefined
-   Number
-   BigInt
-   String
-   Symbol
-   Object: object và Array (Reference Type)

## #4 - Một số hàm built-in function

-   console
-   alert
-   confirm
-   prompt
-   setInterval()
-   setTimeout()

## #5 - Các loại toán tử

```js
Toán tử số học: +, -, *, /, %, **
Toán tử gán: =, +=, -=, *=, /=, %=, **=
Toán tử một ngôi: ++, --
Toán tử tử so sánh: ==, ===, >, >=, <, <=, !=, !==
Toán tử logic: ||, &&, !, !!
Toán tử 3 ngôi: <dieuKien> ? <true> : <false>
```

**Nhóm giá trị truthy và falsy**

-   Falsy: 0, NaN, undefined, null, '', false,
-   Truthy: Ngoài trừ các giá trị trên, tất cả còn lại đều là truthy.

## #6 - Câu lệnh điều kiện và rẽ nhánh

#### Câu lệnh điều kiện if

**Câu lệnh thiếu**

```js
if(<dieuKien>) {
    // do something...
}
```

**Câu lệnh điều kiện đủ**

```js
if(<dieuKien>) {
    // do something...
} else {
    // do something...
}
```

#### Câu lệnh rẽ nhánh và từ khóa break:

```js
switch (value) {
    case 1:
        // do something 1
        break;
    case 2:
        // do something 2
        break;
    case n:
        // do something n
        break;
    default:
    // do someting
}
```

## #7 - Câu lệnh lặp - Từ khóa break và continue

**Vòng lặp for**

```js
for(giaTriKhoiTao, dieuKien, capNhatBienLap) {
    // do something...
}
```

**Vòng lặp while**

```js
while (dieuKien) {
    // do something...
}
```

**Vòng lặp do while**

```js
do {
    // do something
} while (dieuKien);
```

## #8 - Hàm trong Javascript

#### Hàm là gì?

Hàm là một tập hợp các lệnh nhằm thực hiện một chức năng nào đó. (Mỗi hàm chỉ làm 1 nhiệm vụ nhất định).

**Các thành phần cấu tạo nên hàm:**

```js
// Hàm không có tham số, không có giá trị trả về
function sayHello() {
    console.log('Hello Javascript');
}

// Hàm có tham số nhưng không có giá trị trả về
function sayHelloV2(name) {
    console.log('Hello ' + name);
}

// Hàm có tham số và có giá trị trả về
function calcSum(numberA, numberB) {
    return numberA + numberB;
}
```

**Các loại hàm trong Javascript**

-   Declartion function
-   Expression function
-   Arrow function
-   IIFE function
-   Generator function

## #9 - Làm việc với Number

**Chuyển đổi từ chuỗi sang số**

Cách 1:

```js
let str1 = '123';
Number(str1); // 123
let str2 = '123a';
Number(str2); // NaN
```

Cách 2:

```js
let myNumber = +'1234';
```

**Một số built-in có sẵn:**

```js
// parseInt() => Chuyển từ chuỗi sang số nguyên
console.log(Number.parseInt('123')); // 123
console.log(Number.parseInt('123.5a')); // 123

// parseFloat() => Chuyển từ chuỗi sang số thực
console.log(Number.parseFloat('123')); // 123
console.log(Number.parseFloat('123.a5a')); // 123
console.log(Number.parseFloat('123.5a')); // 123.5

// toFixed() => Làm tròn số chữ số và chuyển số về chuỗi
let number1 = 123.5828;
console.log(number1.toFixed(1)); // "123.6" => 8 > 5 <=> 6
console.log(number1.toFixed(2)); // "123.58" => 8 > 5 <=> 6
let number2 - 123.5896
console.log(number2.toFixed(3)); // "123.590" => 6 lấy 3 chữ số gặp số 9 => 590

console.log(number2.toFixed()) // 123
console.log(number2.toFixed(0)) // 123
```

**Một số hàm về toán học**

```js
// Math.sqrt() => tính căn bậc 2
// Math.PI => Lấy số PI
// Math.abs() => lấy trị tuyệt đối
// Math.pow() => Tính lũy thừa
// Math.random() => Tạo số ngẫu nhiên trong khoảng từ 0 => 1
// Math.trunc() => Lấy phần nguyên
let number = 12.345;
console.log(Math.trunc(number)); // 12

// Math.ceil() => Lấy số nguyên và làm tròn lên
console.log(Math.ceil(3.52)); // 4
console.log(Math.ceil(7.1)); // 8

// Math.floor() => Lấy số nguyên và làm tròn xuống
console.log(Math.floor(3.52)); // 3
console.log(Math.floor(7.1)); // 7

// Math.round() => Làm tròn tới số nguyên gần nhất. Phần thập phân lớn hơn hoặc bằng 5 thì tăng, nhỏ hơn 5 thì giảm
console.log(Math.round(3.52)); // 4
console.log(Math.round(7.1)); // 7
console.log(Math.round(5.58)); // 6
```

## #10 - Làm việc với String

**Thao tác cơ bản**

```js
// Lấy ký tự tại vị trí index
let str = 'Javascript number';
// Cách 1
console.log(str.charAt(1)); // a
// Cách 2
console.log(str[0]); // J

// Nối chuỗi
// Cách 1: str = str1 + " " + str2
// Cách 2: str1.concat(" ", str2)
// Cách 3: str = `${str1} ${str2}`

// Duyệt chuỗi: Sử dụng vòng lặp

// Chuyển đổi kiểu chữ:
/*
- Chuyển sang chữ hoa: str.toUpperCase()
- Chuyển sang chữ thường: str.toLowerCase()
*/
```

**Tìm kiếm chuỗi con**

```js
/*
- str.indexOf(strSearch): Trả về vị trí đầu tiên được tìm thấy
- str.lastIndexOf(strSearch): Trả về vị trí đầu tiên được tìm thấy nhưng bắt đầu từ cuối chuỗi
*/
```

**Kiểm tra chuỗi con**

```js
/*
- str.startsWith(strSearch): Kiểm tra chuỗi có được bắt đầu bằng chuỗi cần tìm hay không
- str.endsWith(strSearch): Kiểm tra chuỗi có được kết thúc bằng chuỗi cần tìm hay không
- str.includes(strSearch): Kiểm tra chuỗi có chứa chuỗi cần tìm hay không
=> Có phân biệt chữ hoa và chữ thường
*/
```

**Trích xuất chuỗi con**

```js
/*
- str.slice(strart, end): Lấy chuỗi bắt đầu từ vị trí start đến vị trí end (Nhưng không bao gồm end). Nếu truyền vào số âm, nó sẽ bắt đầu từ cuối chuỗi trở về trước
- str.substring(strart, end): Nếu truyền số âm nó sẽ là 0. Nếu start lớn hơn end nó sẽ tự đảo ngược lại
*/
```

**Tìm kiếm và thay thế**

```js
/*
str.replace(strSearch, strReplace)
str.replaceAll(strSearch, strReplace)
*/
```

**Tách và nối chuỗi**

```js
/*
- split(): Cắt chuỗi thành mảng
- join(): Nối mảng thành chuỗi
*/
```

## #12 - Làm việc với Array

## #13 - Làm việc với Object

## #14 - Tổng kết

## Bài tập Javascript

1. Nhập vào 1 số, kiểm tra số đó có phải là số chẵn hay không?
2. Viết hàm nhập vào điểm của một học sinh và in ra kết quả tương ứng nếu: - Điểm lớn hơn 8 thì in ra **Excellence** - Điểm từ 7 đến 8 thì in ra **Good** - Điểm từ 4 - 6 thì in ra **Not Good** - Nhỏ hơn 4 thì in ra **Bad**

    > Lưu ý: Viết thành nhiều cách càng tốt (Sử dụng câu lệnh điều kiện và cả câu lệnh rẽ nhánh)

3. Cho 1 danh sách sách status code và lỗi trả về từ server như sau: - Nếu 200 trả về: Request successfully - Nếu 201 trả về: Create successfully - Nếu 404 trả về: Not found! - Nếu 403 trả về: Forbidden - Nếu 500 trả về: Sever error! - Nếu không nằm trong các lỗi trên thì trả về: Something went wrong

    > Viết hàm nhận vào 1 lỗi và trả về lỗi tương ứng đó.

4. Viết hàm random một số ngẫu nhiên từ 1 đến n
5. Viết hàm random một số ngẫu nhiên từ a đến b
6. Viết hàm kiểm tra số đó có phải số chẵn hay lẻ
    - Nếu là số chẵn thì trả về **true**
    - Nếu là số lẻ thì trả về **false**
7. Viết hàm kiểm tra số đó có chia hết cho 5 hay không?
8. Viết hàm kiểm tra số đó có phải là số chính phương hay không?
9. Tìm số lớn nhất của 1 số nguyên dương. Điều kiện số đó phải lớn hơn hoặc bằng 0 hoặc nhỏ hơn 1000. Nếu không nằm trong khoảng đó thì trả về **-1**
10. Viết hàm so sánh 2 số nguyên. Nếu:
    - a > b thì trả về 1
    - a < b thì trả về -1
    - a == b thì trả về 0
11. Viết hàm kiểm tra số có tối đa 3 chữ số có phải là số đối xứng hay không?
    > Số đối xứng là số đọc từ trái qua phải cũng giống từ phải qua trái. Ví dụ: 11, 121, 353, 191
12. Viết hàm nhập vào 1 chuỗi và chuẩn hóa chuỗi theo định dạng chữ cái đầu tiên của chuỗi phải được in hoa. Các chữ còn lại viết thường. Ví dụ: HOC lập TRình JavAScript thì phải chuyển thành: **Học lập trình Javascript**
13. Viết hàm kiểm tra trong chuỗi có chứa email **@gmail.com** hay không? Ví dụ:
    - "Liên hệ với chúng tôi cfdtraining@gmail.com" => true
    - "Email của tôi trieunt @ gmail.co" => false
14. Viết hàm nhập vào 1 chuỗi và chuyển đổi chuỗi thành path URL. Ví dụ:

    - "javascript cho nguoi moi bat dau" => **javascript-cho-nguoi-moi-bat-dau**
    - "Hoc JavaSript" => **hoc-javascript**

15. Viết hàm định dạng số giây luôn có 2 chữ số. Ví dụ:

    - Nếu người dùng nhập vào: 12 => 12
    - Nếu người dùng nhập vào: 5 => 05

16. Viết hàm trích xuất domain như sau. Ví dụ: - Nếu là cfdcircle@gmail.com => "gmail.com" - Nếu là learning@cfdcircle.vn => "cfdcircle.vn"
    > Làm theo nhiều cách
