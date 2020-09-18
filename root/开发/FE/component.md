#### 组件类型

1. 容器组件 含有`<ng-content></ng-content>`
2. 输入型组件 含有`@Input()`
3. 输出型组件 含有`@Output()`
4. 输入输出型组件 同时含有`@Input() @Output()`
5. 自闭型组件 设置为`changeDetection: ChangeDetectionStrategy.OnPush`,只能通过 Input 通知它,可触发父组件 check 钩子
6. 父组件 有子组件的组件
7. 普通组件 无以上特征

#### 本项目需自己开发的组件