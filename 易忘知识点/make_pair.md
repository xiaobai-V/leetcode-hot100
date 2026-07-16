

```cpp
#include <utility>
// 也可以用 #include <vector> / <map> 自带
using namespace std;

// 格式：pair<类型1,类型2> 变量名
pair<int, int> p1;
pair<string, double> p2;

// 1. 直接赋值
p1.first = 10;
p1.second = 20;

// 2. 构造初始化
pair<int,int> p3(1,2);

// 3. make_pair 快速创建
auto p4 = make_pair(5,6);

// 4. C++11 简写
pair<int,int> p5 = {3,4};

cout << p1.first;   // 第一个元素
cout << p1.second;  // 第二个元素

swap(p1, p3);
// 比较（默认先比 first，相等再比 second
if(p1 < p3) {}
if(p1 == p3) {}
// 数组 /vector 存 pair
vector<pair<int,int>> v;
v.push_back({1,99});
//  解构赋值 C++17
auto [a,b] = p1;
```