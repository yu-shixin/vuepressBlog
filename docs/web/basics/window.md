# 浏览器操作
## 1. 复制内容到剪切板

```
该方法使用 navigator.clipboard.writeText 来实现将文本复制到剪贴板：
const copyToClipboard = (text) => navigator.clipboard.writeText(text);

copyToClipboard("Hello World");
```

## 2. 清除所有cookie

```
该方法可以通过使用 document.cookie 来访问 cookie 并清除存储在网页中的所有 cookie：
const clearCookies = document.cookie.split(';').forEach(cookie => document.cookie = cookie.replace(/^ +/, '').replace(/=.*/, `=;expires=${new Date(0).toUTCString()};path=/`));
```

## 3. 获取选中的文本

```
该方法通过内置的 getSelection 属性获取用户选择的文本：
const getSelectedText = () => window.getSelection().toString();
getSelectedText();
```

## 4. 检测是否是黑暗模式

```
该方法用于检测当前的环境是否是黑暗模式，它是一个布尔值：
const isDarkMode = window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches
console.log(isDarkMode)
```

## 5. 滚动到页面顶部

```
该方法用于在页面中返回顶部：
const goToTop = () => window.scrollTo(0, 0);
goToTop();
```

## 6. 判断当前标签页是否激活

```
该方法用于检测当前标签页是否已经激活：
const isTabInView = () => !document.hidden;
```

## 7. 判断当前是否是苹果设备

```
该方法用于检测当前的设备是否是苹果的设备：
const isAppleDevice = () => /Mac|iPod|iPhone|iPad/.test(navigator.platform);
isAppleDevice();
```

## 8. 是否滚动到页面底部

```
该方法用于判断页面是否已经底部：
const scrolledToBottom = () => document.documentElement.clientHeight + window.scrollY >= document.documentElement.scrollHeight;
```

## 9. 重定向到一个URL

```
该方法用于重定向到一个新的URL：
const redirect = url => location.href = url
redirect("https://www.google.com/")
```

## 10. 打开浏览器打印框

```
该方法用于打开浏览器的打印框：
const showPrintDialog = () => window.print()
```