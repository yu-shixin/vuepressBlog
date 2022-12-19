# 其他操作
## 1. 随机布尔值

```
该方法可以返回一个随机的布尔值，使用Math.random()可以获得0-1的随机数，与0.5进行比较，就有一半的概率获得真值或者假值。
const randomBoolean = () => Math.random() >= 0.5;
randomBoolean();
```

## 2. 变量交换

```
可以使用以下形式在不适用第三个变量的情况下，交换两个变量的值：
[foo, bar] = [bar, foo];
```

## 3. 获取变量的类型

```
该方法用于获取一个变量的类型：
const trueTypeOf = (obj) => Object.prototype.toString.call(obj).slice(8, -1).toLowerCase();
trueTypeOf('');     // string
trueTypeOf(0);      // number
trueTypeOf();       // undefined
trueTypeOf(null);   // null
trueTypeOf({});     // object
trueTypeOf([]);     // array
trueTypeOf(0);      // number
trueTypeOf(() => {});  // function
```

## 4. 华氏度和摄氏度之间的转化

```
该方法用于摄氏度和华氏度之间的转化：
const celsiusToFahrenheit = (celsius) => celsius * 9/5 + 32;
const fahrenheitToCelsius = (fahrenheit) => (fahrenheit - 32) * 5/9;
celsiusToFahrenheit(15);    // 59
celsiusToFahrenheit(0);     // 32
celsiusToFahrenheit(-20);   // -4
fahrenheitToCelsius(59);    // 15
fahrenheitToCelsius(32);    // 0
```

## 5. 检测对象是否为空

```
该方法用于检测一个JavaScript对象是否为空：
const isEmpty = obj => Reflect.ownKeys(obj).length === 0 && obj.constructor === Object;
```