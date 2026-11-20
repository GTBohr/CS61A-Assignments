# class4 课堂练习：指针与迭代器

C++ 第 4 讲课堂练习，共 8 题，每题一个可独立编译的源文件。

## 文件一览

| 文件 | 主题 | 内容 |
|---|---|---|
| [class4_practice1.cpp](class4_practice1.cpp) | 指针算术 | `short` 数组中 `p1++` / `p1--` 后解引用，验证每步移动 `sizeof(short)` 字节；第二段演示越界访问（未定义行为，输出不可依赖） |
| [class4_practice2.cpp](class4_practice2.cpp) | 指针相减与强转 | `p2 - p1` 得 4；同样的两个地址用 `long*` 视角相减得 1，说明相减结果的单位由指针类型决定 |
| [class4_practice3.cpp](class4_practice3.cpp) | 形参与实参 | 数组作实参传给 `int*` 形参并按格式打印；注释记录 const 形参的只读约束 |
| [class4_practice4.cpp](class4_practice4.cpp) | 迭代器与 vector | `min_element` 返回迭代器而非元素；`erase` 删除元素并前移后续元素，循环把最小的 i 个元素移到末尾 |
| [class4_practice5.cpp](class4_practice5.cpp) | 指针保存地址 | 变量 `a` 改值后通过 `*p` 读到新值，说明指针存的是地址而非快照 |
| [class4_practice6.cpp](class4_practice6.cpp) | 结构体与默认参数 | 成员变量的指针、默认参数 `pi = 3.14`，计算圆面积 |
| [class4_practice7.cpp](class4_practice7.cpp) | 字符串与指针 | 用 `const char*` 遍历 `string::c_str()`，统计非空格字符个数 |
| [class4_practice8.cpp](class4_practice8.cpp) | 递归 | 递归求斐波那契（从 1、2 起步）与递归反转字符串 |

## 编译与运行

```bash
cd HW/hw04/class4
clang++ -std=c++17 class4_practice1.cpp -o practice1
./practice1
```

## 涉及知识点

- 指针算术：加减单位是指向类型的大小，不是 1 字节
- 数组名退化为首元素地址、指针相减、指针强转
- 形参是调用时用实参初始化的局部变量
- `const int*`（内容只读）与 `int* const`（指针只读）的区别
- STL 迭代器、`min_element`、`vector::erase` 后的迭代器失效
- 结构体成员访问与函数默认参数
- 递归的基线条件与递归步
