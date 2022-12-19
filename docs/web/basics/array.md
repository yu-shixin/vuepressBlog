# 数组处理
## 1. 从数组中移除重复项
```javascript
该方法用于移除数组中的重复项：
const removeDuplicates = (arr) => [...new Set(arr)];
console.log(removeDuplicates([1, 2, 2, 3, 3, 4, 4, 5, 5, 6]));
```
## 2. 判断数组是否为空
```javascript
该方法用于判断一个数组是否为空数组，它将返回一个布尔值：
const isNotEmpty = arr => Array.isArray(arr) && arr.length > 0;
isNotEmpty([1, 2, 3]);  // true
```
## 3. 合并两个数组

```
可以使用下面两个方法来合并两个数组：
const merge = (a, b) => a.concat(b);
const merge = (a, b) => [...a, ...b];	
```

## 4.寻找数组中的最大和最小值

```
const arr = [2, 8, 15, 4];
Math.max(...arr); 
Math.min(...arr); 
```

## 5. 初始化数组

如果想要初始化一个指定长度的一维数组，并指定默认值，可以这样：

```
const array = Array(6).fill(''); 
// ['', '', '', '', '', '']
```

如果想要初始化一个指定长度的二维数组，并指定默认值，可以这样：

```
const matrix = Array(6).fill(0).map(() => Array(5).fill(0)); 
// [[0, 0, 0, 0, 0],
//  [0, 0, 0, 0, 0],
//  [0, 0, 0, 0, 0],
//  [0, 0, 0, 0, 0],
//  [0, 0, 0, 0, 0],
//  [0, 0, 0, 0, 0]]
```

## 6. 数组求和、求最大值、最小值

```
const array  = [5,4,7,8,9,2];
```

### 1).数组求和：

```
array.reduce((a,b) => a+b);
```

### 2).数组最大值：

```
1、array.reduce((a,b) => a > b ? a : b);
2、Math.max(...array)
```

### 3).数组最小值：

```
1、array.reduce((a,b) => a < b ? a : b);
2、Math.min(...array)
```

使用数组的 reduce 方法可以解决很多数组的求值问题。

## 7. 过滤错误值

如果想过滤数组中的 false、0、null、undefined 等值，可以这样：

```
const array = [1, 0, undefined, 6, 7, '', false];

array.filter(Boolean);
// [1, 6, 7]
```

## 8. 清空数组

如果想要清空一个数组，可以将数组的 length 置于 0:

```
let array = ["A", "B", "C", "D", "E", "F"]
array.length = 0 
console.log(array)  // []
```

## 9. 拼接数组

如果我们想要拼接几个数组，可以使用扩展运算符：

```
const start = [1, 2] 
const end = [5, 6, 7] 
const numbers = [9, ...start, ...end, 8] // [9, 1, 2, 5, 6, 7 , 8]
```

或者使用数组的 concat() 方法：

```
const start = [1, 2, 3, 4] 
const end = [5, 6, 7] 
start.concat(end); // [1, 2, 3, 4, 5, 6, 7]
```

但是使用 concat() 方法时，如果需要合并的数组很大，那么 concat() 函数会在创建单独的新数组时消耗大量内存。这时可以使用以下方法来实现数组的合并：

```
Array.prototype.push.apply(start, end)
```

通过这种方式就能在很大程度上较少内存的使用。

## 10. 数组元素转化为数字

如果有一个数组，想要把数组中的元素转化为数字，可以使用 map 方法来实现：

```
const array = ['12', '1', '3.1415', '-10.01'];
array.map(Number);  // [12, 1, 3.1415, -10.01]
```

通过这种方式，map 会在遍历数组时，对数组的每个元素执行 Number 构造函数并返回结果。

## 11. 类数组转为数组

可以使用以下方法将类数组 arguments 转化为数组：

```
Array.prototype.slice.call(arguments);
```

除此之外，还可以使用扩展运算符来实现：

```
[...arguments]
```

## 12. 删除数组元素

如果我们想删除数组中的一个元素，我们可以使用 delete 来实现，但是删除完之后的元素会变为 undefined，并不会消失，并且执行时会消耗大量的时间，这样多数情况下都不能满足我们的需求。所以可以使用数组的 splice() 方法来删除数组元素：

```
const array = ["a", "b", "c", "d"] 
array.splice(0, 2) // ["a", "b"]
```

## 13. 获取数组中的最后一项

如果想获取数组中的最后一项，很多时候会这样来写：

```
const arr = [1, 2, 3, 4, 5];
arr[arr.length - 1]  // 5
```

其实我们还可以使用数组的 slice 方法来获取数组的最后一个元素：

```
arr.slice(-1)
```

当我们将 slice 方法的参数设置为负值时，就会从数组后面开始截取数组值，如果我们想截取后两个值，参数传入 - 2 即可。

## 14.将一个数组分成几个数组

```javascript
// array需要分割的数组，subGroupLength每个数组的长度
// 返回值 [[1,2],[3,4]]
group (array, subGroupLength) {
    let index = 0;
    let newArray = [];
    while (index < array.length) {
        newArray.push(array.slice(index, index += subGroupLength));
    }
    return newArray;
}
```

## 15.对数据进行分组

```javascript
//data是要被分组的数据[]，key是分组依据的关键字
let getGroup=(data,key)=>{
    let groups={};
    data.forEach(c=>{
        let value=c[key];
        groups[value]=groups[value]||[];
        groups[value].push(c);
    });
    return groups;
}
```

示例：

```javascript
let data = [
    { key: 'xxx', name: 'yiyi', age: 12, money: 10 },
    { key: 'sss', name: 'iii', age: 13, money: 100 },
    { key: 'ddd', name: 'ooo', age: 13, money: 50 },
    { key: 'sss', name: 'mmm', age: 50, money: 90 },
    { key: 'ddd', name: '888', age: 13, money: 88 },
    { key: 'aaa', name: 'qqq', age: 30, money: 78 },
    { key: 'aaa', name: 'qqq', age: 13, money: 32 },
    { key: 'xxx', name: 'heh', age: 13, money: 95 },
    { key: 'sss', name: 'rtt', age: 15, money: 456 },
    { key: 'xxx', name: 'opp', age: 15, money: 91 },
    { key: 'ddd', name: 'gun', age: 19, money: 66 },
];
console.log(getGroup(data,'key'))
返回值：
{
    aaa:[
        {key: "aaa", name: "qqq", age: 30, money: 78},
        {key: "aaa", name: "qqq", age: 13, money: 32}
    ],
    ddd:[
        {key: "ddd", name: "ooo", age: 13, money: 50},
        {key: "ddd", name: "888", age: 13, money: 88},
        {key: "ddd", name: "gun", age: 19, money: 66}
    ],
    sss:[
        {key: "sss", name: "iii", age: 13, money: 100},
        {key: "sss", name: "mmm", age: 50, money: 90},
        {key: "sss", name: "rtt", age: 15, money: 456}
    ],
    xxx:[
        {key: "xxx", name: "yiyi", age: 12, money: 10}
        {key: "xxx", name: "heh", age: 13, money: 95}
        {key: "xxx", name: "opp", age: 15, money: 91}
    ]
}
```

## 16.数组元素交换位置
```javascript
/**
  * 数组元素交换位置
  * @param {array} arr 数组
  * @param {number} index1 添加项目的位置
  * @param {number} index2 删除项目的位置
  * index1和index2分别是两个数组的索引值，即是两个要交换元素位置的索引值，如1，5就是数组中下标为1和5的两个元素交换位置
  */
swapArray (arr, index1, index2) {
  arr[index1] = arr.splice(index2, 1, arr[index1])[0];
  return arr;
}
```