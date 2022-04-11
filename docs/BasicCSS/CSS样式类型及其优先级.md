## CSS 样式类型及其优先级

通过 CSS 来设置 HTML 元素的样式有三种方式，分别为内联式样式、嵌入式样式、外联式样式。

### 外联式样式

外联样式表通过把 CSS 代码写在一个单独的外部文件中，文件以 `.css` 作为扩展名。然后再 `<head>` 内使用 `<link>` 标签将其链接到 HTML 文件内，以修改元素样式。

```html
<link href="file.css" rel="stylesheet" type="text/css"/>
```

其中 `file.css` 为 CSS 文件的**路径**。而 `rel="stylesheet" type="text/css"`  为固定写法，暂时不必深究。

### 内联式样式

内联式 CSS 样式表即把 CSS 代码直接写在 HTML 标签中。

```html
<h1 style="color: red;">Title</h1>
```

注意：CSS 代码要写在 `style` 属性中，多条 CSS 语句中间用 `;` 隔开。

### 嵌入式样式

嵌入式样式将代码写在 `<style type="text/css"></style>` 标签内，并且，`<style>` 标签一般在 `<head>` 标签内部。

```html
<style type="text/css">
    h1 {
        color: red;
        font-size: 10px;
    }
</style>
```

### 优先级

一般而言，内联式 > 嵌入式 > 外联式。

!> 嵌入式 \> 外联式的前提是嵌入式的代码位置在外联式的后面。