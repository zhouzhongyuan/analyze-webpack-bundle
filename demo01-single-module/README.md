# 打包单一模块

`dist/main.js`其实就是一个立即执行函数，简化如下
```javascript
(function(module){})([function (){},function() {}])
```

### 自执行的匿名函数
1. 声明了 一个变量`installedModules` 和 一个函数`__webpack_require__`，并为`__webpack_require__`添加了`m, c, p`三个属性;
2. 执行`__webpack_require__`，参数为0，并将执行结果返回