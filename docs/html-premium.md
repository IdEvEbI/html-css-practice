# HTML 进阶篇

## 一. 列表

> 笔记对应视频：[P24 ~ P26](https://www.bilibili.com/video/BV1Kg411T7t9?p=24)。

### 01. 列表使用场景和种类

1. 场景：在网页中按照行展示关联性的内容，如：新闻列表、排行榜、账单等
2. 特点：按照行的方式，整齐显示内容
3. 种类：无序列表、有序列表、自定义列表

### 02. 无序列表

1. 场景：在网页中表示一组无顺序之分的列表，如：新闻列表
2. 标签组成：

   | 标签名 | 说明                                       |
   | ------ | ------------------------------------------ |
   | ul     | 表示无序列表的整体，用于包裹 li 标签       |
   | li     | 表示无序列表的每一项，用于包含每一项的内容 |

3. 显示特点：列表的每一项前默认显示**圆点**标识
4. 注意点：
   1. `ul` 标签中只允许包含 `li` 标签
   2. `li` 标签可以包含任意内容

示例代码如下：

```html
<h2>无序列表 - 水果列表</h2>
<ul>
  <li>榴莲</li>
  <li>香蕉</li>
  <li>苹果</li>
  <li>哈密瓜</li>
  <li>火龙果</li>
</ul>
```

### 03. 有序列表

1. 场景：在网页中表示一组有顺序之分的列表，如：排行榜
2. 标签组成：

   | 标签名 | 说明                                       |
   | ------ | ------------------------------------------ |
   | ol     | 表示有序列表的整体，用于包裹 li 标签       |
   | li     | 表示有序列表的每一项，用于包含每一项的内容 |

3. 显示特点：列表的每一项前默认显示**序号**标识
4. 注意点：
   1. `ol` 标签中只允许包含 `li` 标签
   2. `li` 标签可以包含任意内容

示例代码如下：

```html
<h2>有序列表 - 成绩排行榜</h2>
<ol>
  <li>小美：100分</li>
  <li>小帅：80分</li>
  <li>小宝：60分</li>
</ol>
```

### 04. 自定义列表

1. 场景：在网页的底部导航中通常会使用自定义列表实现
2. 标签组成：

   | 标签名 | 说明                                         |
   | ------ | -------------------------------------------- |
   | dl     | 表示自定义列表的整体，用于包裹 dt/dd 标签    |
   | dt     | 表示自定义列表的主题，通常只写一个           |
   | dd     | 表示自定义列表的每一项，一个主题对应多条描述 |

3. 显示特点：dd 前默认显示缩进效果
4. 注意点：
   1. `dl` 标签中只允许包含 `dt/dd` 标签
   2. `dt/dd` 标签可以包含任意内容

示例代码如下：

```html
<h2>自定义列表 - 帮助中心</h2>
<dl>
  <dt>帮助中心</dt>
  <dd>账户管理</dd>
  <dd>购物指南</dd>
  <dd>订单操作</dd>
</dl>
```

## 二. 表格

> 笔记对应视频：[P27 ~ P30](https://www.bilibili.com/video/BV1Kg411T7t9?p=27)。

### 01. 表格基本使用

1. 场景：在网页中以行+列的单元格的方式整齐展示和数据，如：学生成绩表
2. 基本标签：

   | 标签名 | 说明                                            |
   | ------ | ----------------------------------------------- |
   | table  | 表示表格的整体，用于包裹多个 tr（行）标签       |
   | tr     | 表示表格的每一行，用于包裹多个 td（单元格）标签 |
   | td     | 表示表格的单元格，用于包裹内容                  |

3. 常见属性：设置表格基本展示效果

   | 属性名 | 属性值 | 效果     |
   | ------ | ------ | -------- |
   | border | 数字   | 边框宽度 |
   | width  | 数字   | 表格宽度 |
   | height | 数字   | 表格高度 |

   > 提示：实际开发时针对于样式效果推荐用 CSS 设置。

示例代码如下：

```html
<h2>表格基本标签</h2>
<table border="1" width="420" height="320">
  <tr>
    <td>姓名</td>
    <td>成绩</td>
    <td>评语</td>
  </tr>
  <tr>
    <td>小哥哥</td>
    <td>100分</td>
    <td>小哥哥真帅气</td>
  </tr>
  <tr>
    <td>小姐姐</td>
    <td>100分</td>
    <td>小姐姐真漂亮</td>
  </tr>
  <tr>
    <td>总结</td>
    <td>郎才女貌</td>
    <td>郎才女貌</td>
  </tr>
</table>
```

### 02. 表格标题和表头单元格标签

1. 场景：在表格中表示整体大标题（caption）和一列小标题（th）
2. 标签：

   | 标签名  | 说明                                                               |
   | ------- | ------------------------------------------------------------------ |
   | caption | 表示表格整体的大标题，默认在表格顶部居中位置显示                   |
   | th      | 表示表格每一列的小标题，通常用于表格第一行，文字默认加粗并居中显示 |

示例代码如下：

```html
<table border="1">
  <caption>
    <h2>学生成绩单</h2>
  </caption>
  <tr>
    <th>姓名</th>
    <th>成绩</th>
    <th>评语</th>
  </tr>
  <tr>
    <td>小哥哥</td>
    <td>100分</td>
    <td>小哥哥真帅气</td>
  </tr>
  <tr>
    <td>小姐姐</td>
    <td>100分</td>
    <td>小姐姐真漂亮</td>
  </tr>
  <tr>
    <td>总结</td>
    <td>郎才女貌</td>
    <td>郎才女貌</td>
  </tr>
</table>
```

### 03. 表格结构标签

1. 场景：让表格的内容结构分组，突出表格的不同部分(头部、主体、底部)，使语义更加清晰
2. 标签：

   | 标签名 | 说明     |
   | ------ | -------- |
   | thead  | 表格头部 |
   | tbody  | 表格主体 |
   | tfoot  | 表格底部 |

示例代码如下：

```html
<table border="1">
  <caption>
    <h2>学生成绩单</h2>
  </caption>
  <thead>
    <tr>
      <th>姓名</th>
      <th>成绩</th>
      <th>评语</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>小哥哥</td>
      <td>100分</td>
      <td>小哥哥真帅气</td>
    </tr>
    <tr>
      <td>小姐姐</td>
      <td>100分</td>
      <td>小姐姐真漂亮</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>总结</td>
      <td>郎才女貌</td>
      <td>郎才女貌</td>
    </tr>
  </tfoot>
</table>
```

### 04. 合并单元格

1. 场景：将水平或垂直多个单元格合并成一个单元格
2. 步骤：
   1. 明确合并哪几个单元格
   2. 通过左上原则，确定保留谁删除谁
      1. 上下合并 → 只保留最上的，删除其他
      2. 左右合并 → 只保留最左的，删除其他
   3. 给保留的单元格设置：跨行合并（rowspan）或者跨列合并（colspan）

      | 属性名  | 属性值           | 说明                 |
      | ------- | ---------------- | -------------------- |
      | rowspan | 合并单元格的个数 | 从上向下垂直跨行合并 |
      | colspan | 合并单元格的个数 | 从左向右水平跨列合并 |
3. **注意**：不能跨结构标签合并单元格（`thead`、`tbody`、`tfoot`）

示例代码如下：

```html
<table border="1">
  <caption>
    <h2>学生成绩单</h2>
  </caption>
  <thead>
    <tr>
      <th>姓名</th>
      <th>成绩</th>
      <th>评语</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>小哥哥</td>
      <td rowspan="2">100分</td>
      <td>小哥哥真帅气</td>
    </tr>
    <tr>
      <td>小姐姐</td>
      <td>小姐姐真漂亮</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>总结</td>
      <td colspan="2">郎才女貌</td>
    </tr>
  </tfoot>
</table>
```

## 三. 表单

> 笔记对应视频：[P31 ~ P40](https://www.bilibili.com/video/BV1Kg411T7t9?p=31)。

### 01. 表单应用场景

1. 场景：在网页中**收集用户信息**时需要用到表单，例如：**登录**、**注册**、**搜索**等。
2. 标签：`form`

### 02. input 标签

1. 场景：在表单中让用户输入信息，如：用户名、密码、性别等
2. 标签：`input`
3. `type` 属性：`input` 标签的 `type` 属性值不同，展示的效果也不同

   | 标签名 | type 属性值 | 说明                                               |
   | ------ | ----------- | -------------------------------------------------- |
   | input  | text        | 文本框，用于输入单行文本                           |
   | input  | password    | 密码框，用于输入密码                               |
   | input  | radio       | 单选框，用于多选一                                 |
   | input  | checkbox    | 复选框，用于多选多                                 |
   | input  | file        | 文件选择，用于之后上传文件                         |
   | input  | submit      | 提交按钮，用于提交表单                             |
   | input  | reset       | 重置按钮，用于重置表单                             |
   | input  | button      | 普通按钮，默认无功能，之后配合 JavaScript 添加功能 |

示例代码如下：

```html
文本框：<input type="text"><br>
密码框：<input type="password"><br>
单选框：<input type="radio"><br>
复选框：<input type="checkbox"><br>
上传文件：<input type="file"><br>
```

### 03. 文本框占位符

1. 场景：给 `text`（文本框）或 `password`（密码框）增加**提示文字**
2. 属性：`placeholder`

示例代码如下：

```html
账号：<input type="text" placeholder="请输入用户账号"><br>
密码：<input type="password" placeholder="请输入密码">
```

### 04. 单选分组和默认选中

1. 场景：给 `radio`（单选框）或 `checkbox`（复选框）**分组**或**默认选中**
2. 属性：

   | 属性名  | 说明                                                   |
   | ------- | ------------------------------------------------------ |
   | name    | 分组，有相同 name 属性值的**单选框**或**多选框**为一组 |
   | checked | 默认选中                                               |

示例代码如下：

```html
我是 <input type="radio" name="gender"> 男
<input type="radio" name="gender" checked> 女
<br>
婚姻状况 <input type="radio" name="marry" checked> 未婚
<input type="radio" name="marry"> 已婚
<input type="radio" name="marry"> 离异
<br>
<input type="checkbox" checked> 我同意
```

### 05. 上传多个文件

1. 场景：允许 `file`（上传文件）**能够上传多个文件**
2. 属性：

   | 属性名   | 说明             |
   | -------- | ---------------- |
   | multiple | 允许上传多个文件 |

示例代码如下：

```html
上传文件 <input type="file" multiple>
```

### 06. input 按钮

1. 场景：在网页中显示不同功能的按钮，包括：**提交**、**重置**或**普通按钮**
2. `type` 属性：

   | 标签名 | type 属性值 | 说明                                               |
   | ------ | ----------- | -------------------------------------------------- |
   | input  | submit      | 提交按钮，用于提交表单                             |
   | input  | reset       | 重置按钮，用于重置表单                             |
   | input  | button      | 普通按钮，默认无功能，之后配合 JavaScript 添加功能 |

3. 注意：
   1. 如果需要实现按钮功能，需要配合 `form` 标签使用，用 `form` 标签把所有输入控件包裹起来
   2. 使用 `value` 属性可以设置按钮显示的文字

示例代码如下：

```html
<form>
  账户：<input type="text" placeholder="请输入用户账户">
  <br>
  密码：<input type="password" placeholder="请输入用户密码">
  <hr>
  <input type="submit" value="免费注册">
  <input type="reset">
  <input type="button" value="普通按钮">
</form>
```

### 07. button 按钮

1. 场景：在网页中显示不同功能的按钮，包括：**提交**、**重置**或**普通按钮**
2. `type` 属性：

   | 标签名 | type 属性值 | 说明                                               |
   | ------ | ----------- | -------------------------------------------------- |
   | button | submit      | 提交按钮，用于提交表单                             |
   | button | reset       | 重置按钮，用于重置表单                             |
   | button | button      | 普通按钮，默认无功能，之后配合 JavaScript 添加功能 |

3. 注意：
   1. 有些浏览器中 `button` 默认是**提交按钮**
   2. `button` 标签是双标签，更便于包裹其他内容：文字、图片等
   3. 相比较 `input` 按钮，`button` 按钮在开发中更常用

示例代码如下：

```html
<form>
  账户：<input type="text" placeholder="请输入用户账户">
  <br>
  密码：<input type="password" placeholder="请输入用户密码">
  <hr>
  <button>我是按钮</button>
  <button type="submit">提交按钮</button>
  <button type="reset">重置按钮</button>
  <button type="button">普通按钮，没有功能</button>
</form>
```

### 08. 下拉菜单

1. 场景：在网页中提供多个选择项的下拉菜单
2. 标签组成：

   | 标签名 | 说明                                       |
   | ------ | ------------------------------------------ |
   | select | 表示下拉菜单的整体，用于包裹 option 标签   |
   | option | 表示下拉菜单的每一项，用于包含每一项的内容 |

3. 常见属性：`selected` 默认选中下拉菜单中的某一项

示例代码如下：

```html
所在城市：<select>
  <option>北京</option>
  <option>上海</option>
  <option>广州</option>
  <option selected>深圳</option>
</select>
```

### 09. 文本域

1. 场景：在网页中输入多行文本
2. 标签：`textarea`
3. 常见属性：

   | 属性名 | 说明                      |
   | ------ | ------------------------- |
   | cols   | 设置文本域可见列数 → 宽度 |
   | rows   | 设置文本域可见行数 → 高度 |

4. 注意点：
   1. 右下角可以拖拽改变大小
   2. 实际开发时使用 CSS 设置宽高

示例代码如下：

```html
个人简介：<textarea cols="30" rows="10"></textarea>
```

### 10. label 标签

1. 场景：点击标签文字选中对应输入控件，增大点击范围，提升用户体验
2. 标签：`label`
3. 使用方法一：
   1. 使用 `label` 标签把内容（如：文本）包裹起来
   2. 在**表单控件**上添加 `id` 属性
   3. 在 `label` 标签的 `for` 属性中设置对应的 `id` 属性值
4. 使用方法二：
   1. 使用 `label` 标签把内容（如：文本）和**表单控件**一起包裹起来
   2. 把 `label` 标签的 `for` 属性删除即可

示例代码如下：

```html
<h2>方法一：input 和 label 分开</h2>
我是 <input type="radio" name="gender" id="male" checked> <label for="male">男</label>
<input type="radio" name="gender" id="female"> <label for="female">女</label>
<hr>
<h2>方法二：用 label 包裹 input</h2>
婚姻 <label><input type="radio" name="marry" checked>已婚</label>
<label><input type="radio" name="marry">未婚</label>
```

## 四. 其他

## 五. 综合案例
