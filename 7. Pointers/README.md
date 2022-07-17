
# Pointers

Trong bài học này, chúng ta sẽ tìm hiểu về con trỏ, cách chúng ta sử dụng chúng như thế nào và những sai lầm phổ biến mà ta có thể gặp phải khi làm việc với chúng thông qua các ví dụ.

Trước khi tìm hiểu về con trỏ ta hãy tìm hiểu về địa chỉ trong lập trình C

<br />

## What is Address in C?

nếu ta có một biến `num` trong chương trình thì `&num` sẽ là địa chỉ của biến đó trong bộ nhớ

```c
scanf("%d", &num);
```

tại đây giá trị người dùng nhập vào cho biến `num` sẽ được lưu trữ tại địa chỉ của biến `num`.

ví dụ in ra địa chỉ của biến `num`

```c
#include <stdio.h>
int main()
{
  int num = 2;
  printf("num: %d\n", num);
  printf("address of num: %p", &num);  
  return 0;
}
```

kết quả:

```c
num: 2
address of num: 000000000062FE1C
```

> địa chỉ của biến `num` có thể khác trên mỗi máy tính khác nhau

<br />

##  

© Copyright
> ANEST LEARNING  
> Join us: &nbsp;&nbsp;&nbsp; [Facebook groups](https://www.facebook.com/groups/anest.learning/)  
> Website: &nbsp; [https://anest.dev](https://anest.dev)  
