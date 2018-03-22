# Vue组件间通讯

在我们在进行基于[Vue](https://cn.vuejs.org/)的项目开发时，组件间的数据通讯，是我们必须考虑的。

我把组件间的关系，大致分为三种：
1. 父子组件
    ``` html
    <parent>
        <child></child>
    </parent>
    ```
    拥有类似结构，`parent`组件包含`child`组件，则`child`组件是`parent`的父组件，`parent`组件是`child`组件的父组件。
2. 兄弟组件
    ``` html
    <item></item>
    <item></item>
    ```
    两个`item`组件在结构上同级，我们称之互为兄弟组件。
3. 跨多级组件


那么这三种关系的组件，我们应该如何进行组件通讯？

### 数据流

