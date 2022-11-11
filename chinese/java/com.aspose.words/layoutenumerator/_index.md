---
title: LayoutEnumerator
second_title: Aspose.Words for Java API Reference
description: 枚举文档的页面布局实体。
type: docs
weight: 360
url: /zh/java/com.aspose.words/layoutenumerator/
---

**遗产:**
java.lang.Object
```
public class LayoutEnumerator
```

枚举文档的页面布局实体。您可以使用此类来遍历页面布局模型。可用属性包括类型、几何、文本和呈现实体的页面索引，以及整体结构和关系。使用组合[LayoutCollector.getEntity(com.aspose.words.Node)](../../com.aspose.words/layoutcollector\#getEntity-com.aspose.words.Node-)和[getCurrent()](../../com.aspose.words/layoutenumerator\#getCurrent--) / [setCurrent(java.lang.Object)](../../com.aspose.words/layoutenumerator\#setCurrent-java.lang.Object-)移动到对应于文档节点的实体。

要了解更多信息，请访问**Converting to Fixed-page Format**文档文章。
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [LayoutEnumerator(Document document)](#LayoutEnumerator-com.aspose.words.Document-) | 初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(String key)](#get-java.lang.String-) | 获取实体的命名属性。 |
| [get班级()](#get班级--) |  |
| [getCurrent()](#getCurrent--) | 获取页面布局模型中的当前位置。 |
| [getDocument()](#getDocument--) | 获取此实例枚举的文档。 |
| [getKind()](#getKind--) | 获取当前实体的种类。 |
| [getPageIndex()](#getPageIndex--) | 获取包含当前实体的页面的从 1 开始的索引。 |
| [getRectangle()](#getRectangle--) | 返回当前实体相对于页面左上角的边界矩形（以磅为单位）。 |
| [getText()](#getText--) | 获取当前 span 实体的文本。 |
| [get类型()](#get类型--) | 获取当前实体的类型。 |
| [hashCode()](#hashCode--) |  |
| [moveFirstChild()](#moveFirstChild--) | 移动到第一个子实体。 |
| [moveLastChild()](#moveLastChild--) | 移动到最后一个子实体。 |
| [moveNext()](#moveNext--) | 按视觉顺序移动到下一个兄弟实体。 |
| [moveNextLogical()](#moveNextLogical--) | 按逻辑顺序移动到下一个兄弟实体。 |
| [moveParent()](#moveParent--) | 移动到父实体。 |
| [moveParent(int types)](#moveParent-int-) |  |
| [movePrevious()](#movePrevious--) | 移动到上一个兄弟实体。 |
| [movePreviousLogical()](#movePreviousLogical--) | 按逻辑顺序移动到上一个兄弟实体。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [reset()](#reset--) | 将枚举器移动到文档的第一页。 |
| [setCurrent(Object value)](#setCurrent-java.lang.Object-) | 设置页面布局模型中的当前位置。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### LayoutEnumerator(Document document) {#LayoutEnumerator-com.aspose.words.Document-}
```
public LayoutEnumerator(Document document)
```


初始化此类的新实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document) | 要枚举其页面布局模型的文档。

如果尚未建立文档的页面布局模型，则枚举器调用[Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--)建造它。

每当更新文档并创建新的页面布局模型时，都必须使用新的枚举器来访问它。|

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### get(String key) {#get-java.lang.String-}
```
public Object get(String key)
```


获取实体的命名属性。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | java.lang.String | 属性的名称（区分大小写）。 |

**退货:**
java.lang.Object - 如果属性不可用，则为 Null，否则为属性值。这目前用于获取跨度的字体属性。看[Font](../../com.aspose.words/font)可能的属性名称的类。并非所有属性都受支持。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getCurrent() {#getCurrent--}
```
public Object getCurrent()
```


获取页面布局模型中的当前位置。此属性返回对应于当前布局实体的不透明对象。

**退货:**
java.lang.Object - 页面布局模型中的当前位置。
### getDocument() {#getDocument--}
```
public Document getDocument()
```


获取此实例枚举的文档。

**退货:**
[Document](../../com.aspose.words/document) - 记录此实例枚举。
### getKind() {#getKind--}
```
public String getKind()
```


获取当前实体的种类。这可以是一个空字符串，但绝不是 null。这是当前实体的更具体类型，例如书签跨度有[LayoutEntity类型.SPAN](../../com.aspose.words/layoutentitytype\#SPAN)type 并且可以有 BOOKMARKSTART 或 BOOKMARKEND 类型。

**退货:**
java.lang.String - 当前实体的种类。
### getPageIndex() {#getPageIndex--}
```
public int getPageIndex()
```


获取包含当前实体的页面的从 1 开始的索引。

**退货:**
int - 包含当前实体的页面的从 1 开始的索引。
### getRectangle() {#getRectangle--}
```
public Rectangle2D.Float getRectangle()
```


返回当前实体相对于页面左上角的边界矩形（以磅为单位）。

**退货:**
java.awt.geom.Rectangle2D.Float - 当前实体相对于页面左上角的边界矩形（以磅为单位）。
### getText() {#getText--}
```
public String getText()
```


获取当前 span 实体的文本。引发其他实体类型。

**退货:**
java.lang.String - 当前跨度实体的文本。
### get类型() {#get类型--}
```
public int get类型()
```


获取当前实体的类型。

**退货:**
 int - 当前实体的类型。返回值是按位组合[LayoutEntity类型](../../com.aspose.words/layoutentitytype)常数。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### moveFirstChild() {#moveFirstChild--}
```
public boolean moveFirstChild()
```


移动到第一个子实体。

**退货:**
布尔值
### moveLastChild() {#moveLastChild--}
```
public boolean moveLastChild()
```


移动到最后一个子实体。

**退货:**
布尔值
### moveNext() {#moveNext--}
```
public boolean moveNext()
```


按视觉顺序移动到下一个兄弟实体。当迭代跨页中断的段落行时，此方法不会移动到下一页，而是移动到同一页上的下一个实体。

**退货:**
布尔值
### moveNextLogical() {#moveNextLogical--}
```
public boolean moveNextLogical()
```


按逻辑顺序移动到下一个兄弟实体。当迭代跨页中断的段落行时，此方法将移至下一行，即使它位于另一页上。请注意，所有[LayoutEntity类型.SPAN](../../com.aspose.words/layoutentitytype\#SPAN)实体被链接在一起，因此如果[getCurrent()](../../com.aspose.words/layoutenumerator\#getCurrent--) / [setCurrent(java.lang.Object)](../../com.aspose.words/layoutenumerator\#setCurrent-java.lang.Object-)entity is span 重复调用此方法将迭代文档的完整故事。

**退货:**
布尔值
### moveParent() {#moveParent--}
```
public boolean moveParent()
```


移动到父实体。

**退货:**
布尔值
### moveParent(int types) {#moveParent-int-}
```
public boolean moveParent(int types)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| types | int |  |

**退货:**
布尔值
### movePrevious() {#movePrevious--}
```
public boolean movePrevious()
```


移动到上一个兄弟实体。

**退货:**
布尔值
### movePreviousLogical() {#movePreviousLogical--}
```
public boolean movePreviousLogical()
```


按逻辑顺序移动到上一个兄弟实体。当迭代跨页中断的段落行时，此方法将移至上一行，即使它位于另一页上。请注意，所有[LayoutEntity类型.SPAN](../../com.aspose.words/layoutentitytype\#SPAN)实体被链接在一起，因此如果[getCurrent()](../../com.aspose.words/layoutenumerator\#getCurrent--) / [setCurrent(java.lang.Object)](../../com.aspose.words/layoutenumerator\#setCurrent-java.lang.Object-)entity is span 重复调用此方法将迭代文档的完整故事。

**退货:**
布尔值
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### reset() {#reset--}
```
public void reset()
```


将枚举器移动到文档的第一页。

### setCurrent(Object value) {#setCurrent-java.lang.Object-}
```
public void setCurrent(Object value)
```


设置页面布局模型中的当前位置。此属性返回对应于当前布局实体的不透明对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.Object | 页面布局模型中的当前位置。 |

### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
