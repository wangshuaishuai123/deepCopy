一个可以深拷贝的方法，可以对任务类型数据进行深拷贝，如：
基本数据类型（包括 bigint、symbol、undefined、null）、
引用类型（function object arr）、
正则、
错误实例、
日期对象、
等等。

安装：

```js
yarn add npm_deep_copy

//or

npm install npm_deep_copy


```

参数

|                       说明                        | type    | Required |
| :-----------------------------------------------: | ------- | -------- |
| 第一个参数（是否使用深拷贝。默认 false,即浅拷贝） | Boolean | 否       |
|            第二个参数（要拷贝的数据）             | 无限制  | 是       |

使用

```js
import { clone } from "npm_deep_copy";
let obj = {
  name: "shuaishuai",
  age: 12,
  boo: true,
  n: null,
  m: undefined,
  sy: Symbol("xx"),
  child: {
    ele: "body",
    x: 100,
  },
  arr: [10, 20, 30],
  reg: /^\d+$/,
  fn: function () {
    console.log(this.name);
  },
  time: new Date(),
  err: new Error(),
};

clone(true,obj);//深拷贝
```
