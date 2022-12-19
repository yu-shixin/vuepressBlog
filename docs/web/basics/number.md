# 数字操作
## 1. 判断一个数是奇数还是偶数
```
该方法用于判断一个数字是奇数还是偶数：
const isEven = num => num % 2 === 0;
isEven(996);
```
## 2. 获得一组数的平均值
```
const average = (...args) => args.reduce((a, b) => a + b) / args.length;
average(1, 2, 3, 4, 5);   // 3
```
## 3. 获取两个整数之间的随机整数
```
该方法用于获取两个整数之间的随机整数
const random = (min, max) => Math.floor(Math.random() * (max - min + 1) + min);
random(1, 50);
```
## 4. 指定位数四舍五入
```
该方法用于将一个数字按照指定位进行四舍五入：
const round = (n, d) => Number(Math.round(n + "e" + d) + "e-" + d)
round(1.005, 2) //1.01
round(1.555, 2) //1.56
```