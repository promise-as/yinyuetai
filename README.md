# 音悦台

## 头部产品规格

### 总的设计图 `1080px`

- 整个页面背景颜色：`#eeeeee`

### 头部上半部分

- 高度：`135px`

### `logo`部分

- `logo`图片大小：`240px * 88px`
- `logo` 左右内边距：`17px`
  - 上内边距：`26px`
  - 下内边距：`21px`

### 菜单按钮：

- 菜单元素：`129px * 135px`
- 菜单按钮
- 雪碧图大小：`82px * 233px`
- 背景图偏移位置( 关闭 )：`center` `16px`
- 背景图偏移位置( 开启 )：center `-120px`

### 按钮容器：

- 上内边距：`21px`

### 登录/注册按钮：

- 注意 内联元素，需要浮动
- 按钮大小：`111px * 78px`
- 行高：`78px`
- 背景色：`#669900`
- 字体颜色：`#cccccc`
- 右外边距：`15px`
- 字体大小：`42px`
- 文本居中
- 圆角：`8px`

### 小搜索按钮：

- 按钮大小：`130px * 88px`

- 行高：`88px`
- 字体颜色：`#ffffff`
- 右外边距：`30px`
- 上外边距：`3px`
- 字体加粗
- 圆角：`10px`

### 搜索区：

- 高：`103px`
- 上下左右内边距：`16px`

### 输入框：

- 注意`box-sizing`
- 宽( 总 )：`829px`
- 高( 总 )：`103px`
- 背景色：`#999999`
- 上下内边距：`5px`
- 左右内边距：`10px`
- 边距：`1px solid #5a5a5a`
- `input`输入框我们一般都会加`1px`边框
- 字体大小：`41px`
- 字体颜色：`#333333`
- 圆角：`15px`

### 大搜索按钮

- 宽：`203px`
- 高：`103px`
- 边框：`清除边框`
- 背景颜色：`#414040`
- 字体颜色：`#ffffff`
- 字体大小：`41px`
- 圆角：`15px`

### 定位层：

- 高度：`100%`
- 绝对定位`top`：`135px`
- 上下内边距：`10px`
- `上边距`：`1px solid #6a6a6a`
- 背景颜色：`rgba(0, 0, 0, 0.8)`

### 定位层元素：

- 宽度：`22.5%`
- 高度：`135px`
- 行高：`135px`
- 字体大小：`54px`
- 文本居中

## 可拖拽导航产品规格

### 整个内容区域

- `270px` 的头部空隙

### 导航：

- 高度 + 纵向 `padding + border` `177px` ( ` box-sizing`)
- `border`：`1`
- `padding`：上 `31px` 下 `14px`

### 导航元素(`a`)：

- 高：`129px`
- 左右内边距：`38px`
- 默认字体颜色：`#020202`
- 选中时背景颜色：`#669900`
- 选中时字体颜色：`#ffffff`
- 字体大小：`62px`
- 宽度靠内容撑起来

## `tab`切换产品规格

### 省略文本(`css3`)

- 参数
- `clip` 无省略号
- `ellipsis` 省略号( 注意需配合`overflow:hidden`和`white-space:nowarp`一块使用)
- `string` 使用给定的字符串来代替被修剪文体

### 选项卡：

- 整体宽度：`1046px`
- 背景色：`#ffffff`
- 居中
- 头部高度：`135px`
- 头部行高：`135px`

### 导航：

- 行高：`105px`
- 高度：`105px`
- 元素高度：`105px`
- 宽度：`120px`
- 字体大小：`44px`
- 文本居中
- 字体颜色：`#6b6b6b`

底部标识：

- 宽：`120px`
- 高：`9px`
- 背景颜色：`#6f900d`

### 主题内容元素：

- `box-sizing: border-box`
- 宽：`506px`
- 外边距：`8px`
- 内边距：`5px`
- 字体大小：`40px`
- 颜色背景：`#efefef`
- 字体颜色：`#00000`

### `loading`：

- 宽度：`101px`
- 透明度：`0`

## 子节点的获取

### 获取指定节点的所有子节点

- 一共有三种方式
  - `childNodes`属性：
    - 不实用，会取到文本节点
  - `children`属性：
    - 实用，会剔除文本节点
- 用该指定节点的`getElementsByTagName`方法( 注意不是`document`)：
  - 不实用，虽然会剔除文本节点，但只能去一组相同`tagName`的子节点，无法取全
  - `parent.getElementsByTagName("p")`

### 获取第一个或者最后一个子节点

- `firstChild`和`lastChild`
  - 会受到文本子节点的影响
  - 我们通常可以使用`firstChild`的`nodeValue`属性来获取文本值( 当子节点只有文本节点时 )
  - `innerText`
  - `innerHtml`