<style>
    table {
        border-collapse:collapse;
        margin-left:40px;
    }
    tr {
        border:1px solid #ccc;
    }
    td,th {
        padding:5px 10px;
    }
</style>

#### 命名规划

- 函数(动词+名词)

| 动词   | 含义                       | 返回值               |
| ------ | -------------------------- | -------------------- |
| can    | 是否可执行某个动作         | boolean              |
| has    | 含有某个值，该值使原始类型 | boolean              |
| is     | 判断值为某类型             | boolean              |
| get    | 获取某个值，该值为原始类型 | value                |
| set    | 设置某个值，该值为原始类型 | void                 |
| load   | 加载本地资源               | promise / Observable |
| fetch  | 获取服务器中数据           | promise / Observable |
| hand   | 中转一个动作               | any                  |
| create | 增加 this 中数据           | void                 |
| delete | 删除 this 中数据           | void                 |
| update | 修改 this 中数据           | void                 |
| read   | 读取 this 中数据           | void                 |
| backTo | 返回到某个状态             | void                 |
| on     | 绑定 DOM 原生事件          | void                 |

- 常量 = const + 大写名词

- 变量 = let + 小写名词

- 纯净函数 = const + 小写动词/名词

- 类名 = class + 大写首字母的名词
