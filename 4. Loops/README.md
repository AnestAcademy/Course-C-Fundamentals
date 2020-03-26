# Loop

### What is a loop?

Vòng lặp cho phép bạn lặp lại việc thực thi một khối lệnh cho tới khi một điều kiện nhất định được thỏa mãn.

Tùy thuộc vào vị trí của câu lệnh điều kiện trong chương trình, một vòng lặp được phân thành hai loại:
- **Entry controlled loop**  
  Một điều kiện được kiểm tra trước khi thực hiện phần thân của một vòng lặp. Nó cũng được gọi là vòng lặp kiểm tra trước.
- **Exit controlled loop**  
  Một điều kiện được kiểm tra sau khi thực hiện phần thân của một vòng lặp. Nó cũng được gọi là một vòng lặp kiểm tra sau.

Các điều kiện điều phải được xác định rõ ràng và được chỉ định nếu không vòng lặp sẽ chạy vô số lần. Vòng lặp không dừng chạy (hay chạy mãi) được gọi là vòng lặp vô hạn (infinite loop). Sau đây là một số đặc điểm của một vòng lặp vô hạn:
- Không có điều kiện chấm dứt được chỉ định.
- Các điều kiện quy định không bao giờ được đáp ứng.

Ngôn ngữ lập trình C cung cấp cho chúng ta ba loại cấu trúc vòng lặp:
- Vòng lặp `for`
- Vòng lặp `do-while`
- Vòng lặp `while`

## I. `for` loop

Vòng lặp `for` được sử dụng để duyệt qua các phần tử trong một tập hợp. Nó thường được sử dụng khi bạn có một khối câu lệnh cần được thực thi `n` lần, có nghĩa là bạn biết được số lượng vòng lặp cần thực hiện.

### 1. The syntax of the `for` loop

```c
for (khởi tạo giá trị biến lặp; điều kiện lặp; cập nhật biến lặp) {

   // statements inside the body of loop
}
```
### 3. How for loop works?

<p align="center">
  <img src="https://github.com/AnestLearning/Course-C-Fundamentals/blob/master/Images/for-loop-structure.jpg">
</p>

- Bước 1: Khởi tạo giá trị biến lặp, chỉ thực hiện 1 lần duy nhất
- Bước 2: Kiểm tra điều kiện lặp, nếu điều kiện `false` thì kết thúc vòng lặp.
- Bước 3: Tuy nhiên, nếu biểu thức kiểm tra là `true`, các câu lệnh bên trong phần thân của vòng lặp `for` được thực thi.
- Bước 4: Cập nhật giá trị biến lặp và quay trở lại bước 2 để kiểm tra.

Quá trình này diễn ra cho đến khi biểu thức điều kiện kiểm tra là `false`. Khi biểu thức điều kiện kiểm tra là `false`, vòng lặp chấm dứt.

### 4. `for` loop flowchart

<p align="center">
  <img src="https://github.com/AnestLearning/Course-C-Fundamentals/blob/master/Images/c-for-loop.jpg">
</p>

### 5. Example:

```c
#include <stdio.h>
 
int main(){
    for(int i = 0; i < 10; i++){
        printf("Times %d : I am for loop\n", i);
    }
    // Continue ...
    printf("End loop!\n");
}
```
Kết quả:

```c
Times 0 : I am for loop
Times 1 : I am for loop
Times 2 : I am for loop
Times 3 : I am for loop
Times 4 : I am for loop
Times 5 : I am for loop
Times 6 : I am for loop
Times 7 : I am for loop
Times 8 : I am for loop
Times 9 : I am for loop
End loop!

--------------------------------
Process exited after 0.02771 seconds with return value 0
Press any key to continue . . .
```

Giải thích:
- Bước 1. Gán biến lặp i = 0
- Bước 2. Kiểm tra điều kiện (i = 0) < 10 => Đúng
- Bước 3. Do kiểm tra điều kiện đúng => Thực hiện thân vòng lặp for
- Bước 4. Gọi tới (i++) => tăng i lên 1 đơn vị => i = 1
- Bước 5. Quay lại bước 2 và chạy đến khi i = 10
- Bước 6. Kiểm tra điều kiện (i = 10) < 3 => Sai => Kết thúc vòng lặp

## II. while loop

**1. Định nghĩa**

Vòng lặp while được sử dụng để lặp lại một khối lệnh. Thay vì chỉ chạy khối mã nguồn một lần, nó sẽ thực thi khối mã nguồn đó nhiều lần cho tới khi thỏa mãn một điều kiện cho trước.

**2. Cú pháp của vòng lặp while:**

```c
while (testExpression) 
{
    // statements inside the body of the loop 
}
```

**3. Và đây là sơ đồ khối mô tả hoạt động của vòng lặp while:**

<p align="center">
  <img src="https://github.com/AnestLearning/Course-C-Fundamentals/blob/master/Images/c-while-loop_0.jpg">
</p>

- Vòng lặp while kiểm tra biểu thức kiểm tra bên trong dấu ngoặc đơn ().
- Nếu biểu thức kiểm tra là đúng, các câu lệnh bên trong thân vòng lặp while được thực thi. Sau đó, biểu thức kiểm tra được đánh giá lại.
- Quá trình diễn ra cho đến khi biểu thức kiểm tra được đánh giá là sai.
- Nếu biểu thức kiểm tra là sai, vòng lặp chấm dứt (kết thúc).

**4. Ví dụ minh họa vòng lặp while trong C**

```c
// Print numbers from 1 to 5

#include <stdio.h>

int main(){
    int i = 1;
    
    while (i <= 5)
    {
        printf("%d\n", i);
        ++i;
    }

    return 0;
}
```

Kết quả :

```c
Result:
1
2
3
4
5

--------------------------------
Process exited after 0.0269 seconds with return value 0
Press any key to continue . . .
```
Giải thích:
- Khi i là 1, biểu thức kiểm tra i <= 5 là đúng. Do đó, phần thân của vòng lặp while được thực thi. Điều này in 1 trên màn hình và giá trị của i được tăng lên 2.
- Bây giờ, tôi là 2, biểu thức kiểm tra i <= 5 lại đúng. Phần thân của vòng lặp while được thực hiện lại. Điều này in 2 trên màn hình và giá trị của i được tăng lên 3.
- Quá trình này diễn ra cho đến khi i=6. Khi i = 6, biểu thức kiểm tra i <= 5 sẽ sai và vòng lặp chấm dứt.

## III. do...while loop

**1. Định Nghĩa:**

Vòng lặp do.. while tương tự như vòng lặp while với một điểm khác biệt quan trọng. Phần thân của vòng lặp do ... được thực thi ít nhất một lần. Chỉ sau đó, biểu thức kiểm tra được đánh giá.

**2. Cú pháp của vòng lặp do ... while là:**

```c
do
{
   // statements inside the body of the loop
}
while (testExpression);
```
**3. Vòng lặp do...while hoạt động như thế nào?**

Sơ đồ của do...while loop

<p align="center">
  <img src="https://github.com/AnestLearning/Course-C-Fundamentals/blob/master/Images/c-do-while-loop_0.jpg">
</p>

- Phần thân của vòng lặp do ... luôn luôn thực thi một lần. Sau đó, biểu thức kiểm tra mới được đánh giá.
- Nếu biểu thức kiểm tra là đúng, phần thân của vòng lặp được thực hiện lại.
- Quá trình này diễn ra cho đến khi biểu thức kiểm tra trở thành sai.
- Nếu biểu thức kiểm tra là sai, vòng lặp kết thúc.

**4. Ví dụ minh họa vòng lặp do...while trong C**

```c
// Program to add numbers until the user enters zero

#include <stdio.h>

int main() {
    double number, sum = 0;

    // the body of the loop is executed at least once
    do
    {
        printf("Enter a number: ");
        scanf("%lf", &number);
        sum += number;
    }while(number != 0.0);

    printf("Sum = %.2lf",sum);
}
```
Kết quả:

```c
Enter a number: 5.6
Enter a number: 5
Enter a number: 10.2
Enter a number: 0.0
Sum = 20.80
--------------------------------
Process exited after 11.4 seconds with return value 0
Press any key to continue . . .
```
