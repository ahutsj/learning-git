 # 变量
                                                
```go               
var a int //声明一个整型变量
var b string //字符串类型
var c []float32 //32位浮点切片类型的变量，浮点切片表示多个浮点类型组成的数据结构
var d func() bool //返回值为bool类型的函数变量，一般用于回调函数`
var e struct{
     x int
     }//结构体类型的变量，这个结构拥有一个整型的x字段
```

## 变量声明格式
### 1、标准格式
`var  变量名 变量类型`
	 
### 2、批量格式

```go
var (
     a int
     b string
     e struct {
          x int
          }
     ) 
```
## 初始化变量
整型、浮点型默认为0
字符串变量默认是空字符串
bool型默认是bool
切片、函数、指针变量默认是nil

### 1、标准格式

`var 变量名 类型 = 表达式`

### 2、编译器推导

`var hp = 100`

### 3、短变量声明并初始化

`hp := 100//左值变量必须没有被定义过，否则报错（左边至少有一个新变量）`

多重赋值时，变量的左值和右值按照从左到右的顺序赋值：
`b,a = a,b //交换a b的值`

匿名变量：用 “_” 代替变量。匿名变量不占命名空间，不分配内存，匿名变量和匿名变量之间也不会因为多次声明而无法使用

111ceshi