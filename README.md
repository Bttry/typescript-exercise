# typescript-exercise

## 开发环境的安装

> 安装 Node.js

官网下载: https://nodejs.org/zh-cn/download/

> 安装 TypeScript 包

```sh
npm install typescript -g
# 检查typescript是否安装成功
tsc --version
```

> TypeScript 项目的配置文件

```sh
tsc --init
```

## tsconfig.json

```js
{
  // 编译选项
  "compilerOptions": {
    /* 基本配置 */
    // 指定ECMAScript目标版本：'ES3'（默认），'ES5'，'ES2015'，'ES2016'，'ES2017'，'ES2018'或'ESNEXT'
    "target": "es5",
    // 指定模块代码生成：'none'，'commonjs'，'amd'，'system'，'umd'，'es2015'或'ESNext'
    "module": "commonjs",
    // 指定要包含在编译中的库文件
    "lib": [],
    // 允许编译javascript文件
    "allowJs": true,
    // 报告.js文件中的错误
    "checkJs": true,
    // 指定JSX代码生成：'preserve'，'react-native'或'react'
    "jsx": "preserve",
    // 生成相应的 '.d.ts' 文件
    "declaration": true,
    // 为每个对应的 '.d.ts' 文件生成源图
    "declarationMap": true,
    // 生成相应的 '.map' 文件
    "sourceMap": true,
    // 连接并将输出发送到单个文件
    "outFile": "./",
    // 将输出结构重定向到目录
    "outDir": "./",
    // 指定输入文件的根目录。 用于通过--outDir控制输出目录结构
    "rootDir": "./",
    // 启用项目编译
    "composite": true,
    // 删除所有注释，除了以 /!*开头的版权信息
    "removeComments": true,
    // 不生成输出文件
    "noEmit": true,
    // 从 tslib 导入辅助工具函数（比如 __extends， __rest等）
    "importHelpers": true,
    // 在定位 ES5 或 ES3 时，为 for-of，展开和解构中的迭代提供全面支持
    "downlevelIteration": true,
    // 将每个文件作为单独的模块（与“ts.transpileModule”类似）
    "isolatedModules": true,

    /* 严格的类型检查选项 */
    // 启用所有严格类型检查选项 启用 --strict相当于启用 --noImplicitAny, --noImplicitThis, --alwaysStrict， --strictNullChecks和 --strictFunctionTypes和--strictPropertyInitializatio
    "strict": true,
    // 在表达式和声明上有隐含的 any类型时报错
    "noImplicitAny": true,
    // 在严格的 null检查模式下， null和 undefined值不包含在任何类型里，只允许用它们自己和 any来赋值（有个例外， undefined可以赋值到 void）
    "strictNullChecks": true,
    // 禁用函数参数双向协变检查
    "strictFunctionTypes": true,
    // 在函数上启用严格的 'bind', 'call', 和 'apply'方法
    "strictBindCallApply": true,
    // 确保类的非undefined属性已经在构造函数里初始化。若要令此选项生效，需要同时启用--strictNullChecks
    "strictPropertyInitialization": true,
    // 当 this表达式的值为 any类型的时候，生成一个错误
    "noImplicitThis": true,
    // 以严格模式解析并为每个源文件生成 "use strict"语句
    "alwaysStrict": true,

    /* 其他检查 */
    // 若有未使用的局部变量则抛错
    "noUnusedLocals": true,
    // 若有未使用的参数则抛错
    "noUnusedParameters": true,
    // 	不是函数的所有返回路径都有返回值时报错
    "noImplicitReturns": true,
    // 报告switch语句的fallthrough错误。（即，不允许switch的case语句贯穿）
    "noFallthroughCasesInSwitch": true,

    /* 模块解析选项 */
    // 决定如何处理模块。或者是"Node"对于Node.js/io.js，或者是"Classic"（默认）
    "moduleResolution": "node",
    // 解析非相对模块名的基准目录
    "baseUrl": "./",
    // 模块名到基于 baseUrl的路径映射的列表
    "paths": {},
    // 根（root）文件夹列表，表示运行时组合工程结构的内容
    "rootDirs": [],
    // 	要包含的类型声明文件路径列表
    "typeRoots": [],
    // 要包含的类型声明文件名列表
    "types": [],
    // 允许从没有设置默认导出的模块中默认导入。这并不影响代码的输出，仅为了类型检查
    "allowSyntheticDefaultImports": true,
    // 通过为所有导入创建命名空间对象，启用CommonJS和ES模块之间的互操作性。 意味着'allowSyntheticDefaultImports'
    "esModuleInterop": true,
    // 不把符号链接解析为其真实路径；将符号链接文件视为真正的文件
    "preserveSymlinks": true,

    /* 源码图选项 */
    // 指定TypeScript源文件的路径，以便调试器定位。当TypeScript文件的位置是在运行时指定时使用此标记。路径信息会被加到 sourceMap里
    "sourceRoot": "",
    // 	为调试器指定指定sourcemap文件的路径，而不是使用生成时的路径。当 .map文件是在运行时指定的，并不同于 js文件的地址时使用这个标记。指定的路径会嵌入到 sourceMap里告诉调试器到哪里去找它们
    "mapRoot": "",
    // 生成单个sourcemaps文件，而不是将每sourcemaps生成不同的文件
    "inlineSourceMap": true,
    // 将代码与sourcemaps生成到一个文件中，要求同时设置了 --inlineSourceMap或 --sourceMap属性
    "inlineSources": true,

    /* 实验选项 */
    // 启用实验性的ES装饰器
    "experimentalDecorators": true,
    // 给源码里的装饰器声明加上设计类型元数据
    "emitDecoratorMetadata": true
  }
}
```
