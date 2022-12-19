# 数组方法

## concat() 
连接两个或更多的数组，并返回结果。(不会改变原数组)

连接两个数组

```javascript
    let arr1 = [0, 1, 2, 3, 4, 5]
    let arr2 = [6, 7, 8, 9, 10]
    let a = arr1.concat(arr2)
    console.log(a);     // [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

连接三个数组

```javascript
	let arr1 = [0, 1, 2, 3, 4, 5]
    let arr2 = [6, 7, 8, 9, 10]
    let arr3 = [11,12,13,14]
    let a = arr1.concat(arr2,arr3)
    console.log(a);     // [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

## filter() 
检测数值元素，并返回符合条件所有元素的数组。(不会改变原数组)

获取数组中大于3的元素数组

```javascript
    let arr1 = [0, 1, 2, 3, 4, 5]
    let a = arr1.filter(item => {
      return item > 3
    })
    console.log(a);    // [4, 5]
```

## find() 
返回符合传入测试（函数）条件的数组元素。(第一个符合条件的元素)(不会改变原数组)

获取数组中大于3的第一个元素

```javascript
    let arr1 = [0, 1, 2, 3, 4, 5]
    let a = arr1.find(item => {
      return item > 3
    })
    console.log(a);    // 4
```

## findIndex() 
返回符合传入测试（函数）条件的数组元素索引。(第一个符合条件元素索引)(不会改变原数组)

获取数组中大于3的第一个元素索引

```javascript
    let arr1 = [0, 1, 2, 3, 4, 5]
    let a = arr1.findIndex(item => {
      return item > 3
    })
    console.log(a);    // 4
```

## forEach() 
数组每个元素都执行一次回调函数。(循环)

## map() 
通过指定函数处理数组的每个元素，并返回处理后的数组。

```javascript
    let arr1 = [0, 1, 2, 3, 1, 5]
    let a = arr1.map(item => {
      return item + 1
    })
    console.log(a);   // [1, 2, 3, 4, 2, 6]
```

## some() 
检测数组元素中是否有元素符合指定条件。

```javascript
    let arr1 = [0, 1, 2, 3, 1, 5]
    let a = arr1.some(item => {
      return item > 1
    })
    console.log(a);     // true
    console.log(arr1);  // [1, 2, 3, 1, 5]
```

## includes() 
判断一个数组是否包含一个指定的值。

判断 1 是否在 arr1 中

```javascript
	let arr1 = [0, 1, 2, 3, 4, 5]
    let a = arr1.includes(1)
    console.log(a);   // true
```

## indexOf()  
搜索数组中的元素，并返回它首次出现的位置。

获取 1 在 arr1 中的索引位置

```javascript
    let arr1 = [0, 1, 2, 3, 1, 5]
    let a = arr1.indexOf(1)
    console.log(a);   // 1
```

## lastIndexOf() 
搜索数组中的元素，并返回它最后出现的位置。

```javascript
    let arr1 = [0, 1, 2, 3, 1, 5]
    let a = arr1.lastIndexOf(1)
    console.log(a);   // 4
```

## isArray() 
判断对象是否为数组。

```javascript
    let arr1 = [0, 1, 2, 3, 4, 5]
    let a = Array.isArray(arr1)
    console.log(a);   // true
```

## join()  
把数组的所有元素放入一个字符串。

默认用 , 分割

```javascript
    let arr1 = [0, 1, 2, 3, 4, 5]
    let a = arr1.join()
    let b = arr1.join('-')
    console.log(a);   // 0,1,2,3,4,5
    console.log(b);   // 0-1-2-3-4-5
```

## reverse() 
反转数组的元素顺序。（改变原数组）

```javascript
    let arr1 = [0, 1, 2, 3, 1, 5]
    let a = arr1.reverse()
    console.log(a);   // [5, 1, 3, 2, 1, 0]
    console.log(arr1);  // [5, 1, 3, 2, 1, 0]
```

## shift() 
删除并返回数组的第一个元素。(改变原数组)

```javascript
    let arr1 = [0, 1, 2, 3, 1, 5]
    let a = arr1.shift()
    console.log(a);   // 0
    console.log(arr1);  // [1, 2, 3, 1, 5]
```

## pop()  
删除数组的最后一个元素并返回删除的元素。(改变原数组)

```javascript
    let arr1 = [0, 1, 2, 3, 1, 5]
    let a = arr1.pop()
    console.log(a);   // 5
    console.log(arr1);  // [0, 1, 2, 3, 1]
```

## unShift() 
向数组的开头添加一个或更多元素，并返回新的长度。(改变原数组)

```javascript
    let arr1 = [0, 1, 2, 3, 1, 5]
    let a = arr1.unshift(11)
    console.log(a);     // 7
    console.log(arr1);  // [11, 0, 1, 2, 3, 1, 5]
```

## push() 
向数组的末尾添加一个或更多元素，并返回新的长度。（改变原数组）

```javascript
    let arr1 = [0, 1, 2, 3, 1, 5]
    let a = arr1.push(6)
    console.log(a);   // 7
    console.log(arr1);  // [0, 1, 2, 3, 1,5,6]
```

## slice() 
选取数组的一部分，并返回一个新数组。(不改变原数组)

第一个参数为第几个元素开始(不包含当前元素)

```javascript
    let arr1 = [0, 1, 2, 3, 1, 5]
    let a = arr1.slice(3)
    console.log(a);   // [3, 1, 5]
    console.log(arr1);  // [1, 2, 3, 1, 5]
```

第一个参数为负数，则表示从原数组中的倒数第几个元素开始提取(包含当前元素)

```javascript
    let arr1 = [0, 1, 2, 3, 1, 5]
    let a = arr1.slice(-2)
    console.log(a);   // [1, 5]
    console.log(arr1);  // [1, 2, 3, 1, 5]
```

第二个参数为结束元素的索引(不包含当前索引的元素)，如果没有则到末尾

```javascript
    let arr1 = [0, 1, 2, 3, 1, 5]
    let a = arr1.slice(3,5)
    console.log(a);   // [3, 1]
    console.log(arr1);  // [1, 2, 3, 1, 5]
```

第二个参数为负数， 则它表示在原数组中的倒数第几个元素结束抽取。(不包含当前元素)

```javascript
    let arr1 = [0, 1, 2, 3, 1, 5]
    let a = arr1.slice(2,-2)
    console.log(a);   // [2, 3]
    console.log(arr1);  // [1, 2, 3, 1, 5]
```

## sort() 
对数组的元素进行排序。

```javascript
    let arr1 = [0, 1, 2, 3, 1, 5]
    let a = arr1.sort()
    console.log(a);     // [0, 1, 1, 2, 3, 5]
```

## splice()  
从数组中添加或删除元素。(改变原数组)

第一个参数 必需 规定从何处添加/删除元素 索引(包含当前元素)

```javascript
    let arr1 = [0, 1, 2, 3, 1, 5]
    let a = arr1.splice(0)
    console.log(a);     // [0, 1, 2, 3, 1, 5]
    console.log(arr1);  // []
```

第二个参数 删除几个(可以为0)

```javascript
    let arr1 = [0, 1, 2, 3, 1, 5]
    let a = arr1.splice(0,1)	// 从第0个 删除1个
    console.log(a);     // [0]
    console.log(arr1);  // [1, 2, 3, 1, 5]
```

第三个(3+n个)参数 添加的元素

```javascript
    let arr1 = [0, 1, 2, 3, 1, 5]
    let a = arr1.splice(0,1,10)	// 从第0个 删除1个 添加元素在为10
    console.log(a);     // [0]
    console.log(arr1);  // [10, 1, 2, 3, 1, 5]
```

## toString() 
把数组转换为字符串，并返回结果。(不改变原数组)

```javascript
    let arr1 = [0, 1, 2, 3, 1, 5]
    let a = arr1.toString()
    console.log(a);     // 0,1,2,3,1,5
    console.log(arr1);  // [0, 1, 2, 3, 1, 5]
```

