
# BÀI 1: Compiler và Preprocessing
## 1. Macro và Include
### 1.1 #include
đây là chỉ thị dùng để khai báo 1 file nguồn đã được viết sẵn, ta s4 khai báo chỉ thị này cùng với tên của file mà ta cần thêm vào chương trình chính.
+ __#include" "__ : khi file nguồn của chúng ta đặt trong " ", thì chạy chương trình, hệ thống sẽ tìm trong folder của project hiện tại có file đó không và thay thế vào chương trình

+ __#include <>__ : trong trường hợp này thì hệ thống sẽ tìm trong thư mục cài đặt gốc ở bất kỳ đâu trong máy tính để lấy ra file đó

### 1.2 #define 
Đây là chỉ thị để định nghĩa 1 macro, hay nói cách khác ta có thể gán bất kỳ giá trị nào bằng 1 cái tên mà ta định nghĩa thông qua từ khóa #define 

__a) macro nối chuỗi__

__b) macro chuẩn hóa chuỗi__

__c) macro variadic__

## 2. Các chỉ thị tiền xử lý 
### 2.1 #undef, #ifndef, #endif

### 2.2 #if, #elif, #else
__thiết kế thư viện__
## 3. Quá trình biên dịch ra chương trình chạy thực tế
Để 1 chương trình được viết bằng các ngôn ngữ bậc cao như C/C++ chạy được thì sẽ phải trải qua các bước sau. 
### Bước 1: Tiền xử lý (Preprocessing)
Ở giai đoạn này file main.c sẽ được dịch sang file main.i bằng câu lệnh sau

```bash
 gcc -E main.c -o main.i
```
Muc tiêu của bước này sẽ là xuất ra file main.i 
+ thay thế nội dung của các chỉ #include bằng file nguồn mà nó định nghĩa
+ thay thế các chỉ thị #define bằng nội dung mà nó định nghĩa 
+ xóa bỏ các comment trong file main.c 
__Ví dụ__

### Bước 2: biên dịch (compiler)
Lúc này từ file main.s sẽ được biên dịch sang file main.s bằng câu lệnh sau
```bash
 gcc -S main.i -o main.s
```
Mục tiêu của bước này sẽ xuất ra file main.s
+ chứa các dòng code đã được dịch từ ngôn ngữ cấp cao sang hợp ngữ để máy tính có thể hiểu và thực thi ở các bước sau
### Bước 3: dịch sang mã máy (assembler)
+ Từ file main.s sẽ được dịch sang fle main.o bằng câu lệnh sau
```bash
 gcc -c main.s -o main.o
```
Mục tiêu của bước này là xuất ra file main.o
+ chứa các đoạn code đã được mã hóa dưới dạng binary hoặc hex, để máy tính có thể xử lý 
### Bước 4: liên kết (linker)
+ Sau đó ta sẽ liên kết  các file main.o lại thành 1 file duy nhất, hay còn gọi là file exe thông qua câu lệnh sau
```bash
 gcc main.o -o main
 ```
### Bước 5: chạy chương trình
Cuối cùng ta sẽ thực hiện chạy chương trình với file exe vừa sinh ra
```bash
 ./main
 ```



## Installation

Install my-project with npm

```bash
  npm install my-project
  cd my-project
```
    
