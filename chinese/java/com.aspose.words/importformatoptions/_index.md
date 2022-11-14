---
title: ImportFormatOptions
second_title: Aspose.Words for Java API 参考
description: 允许指定各种导入选项来格式化输出。
type: docs
weight: 347
url: /zh/java/com.aspose.words/importformatoptions/
---

**遗产:**
java.lang.Object
```
public class ImportFormatOptions
```

允许指定各种导入选项来格式化输出。

要了解更多信息，请访问**Specify Load Options**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getForceCopyStyles()](#getForceCopyStyles--) | 获取一个布尔值，指示复制冲突的样式[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING)模式。 |
| [getIgnoreHeaderFooter()](#getIgnoreHeaderFooter--) | 获取一个布尔值，该值指定在以下情况下忽略页眉/页脚内容的源格式[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING)使用模式。 |
| [getIgnoreTextBoxes()](#getIgnoreTextBoxes--) | 获取一个布尔值，该值指定忽略文本框内容的源格式，如果[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING)使用模式。 |
| [getKeepSourceNumbering()](#getKeepSourceNumbering--) | 获取一个布尔值，该值指定编号在源文档和目标文档中发生冲突时如何导入。 |
| [getMergePastedLists()](#getMergePastedLists--) | 获取一个布尔值，该值指定是否将粘贴的列表与周围的列表合并。 |
| [getSmartStyleBehavior()](#getSmartStyleBehavior--) | 获取一个布尔值，该值指定样式在源文档和目标文档中具有相同名称时如何导入。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setForceCopyStyles(boolean value)](#setForceCopyStyles-boolean-) | 设置一个布尔值，指示复制冲突的样式[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING)模式。 |
| [setIgnoreHeaderFooter(boolean value)](#setIgnoreHeaderFooter-boolean-) | 设置一个布尔值，指定在以下情况下忽略页眉/页脚内容的源格式[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING)使用模式。 |
| [setIgnoreTextBoxes(boolean value)](#setIgnoreTextBoxes-boolean-) | 设置一个布尔值，指定忽略文本框内容的源格式，如果[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING)使用模式。 |
| [setKeepSourceNumbering(boolean value)](#setKeepSourceNumbering-boolean-) | 设置一个布尔值，用于指定编号在源文档和目标文档中发生冲突时如何导入。 |
| [setMergePastedLists(boolean value)](#setMergePastedLists-boolean-) | 设置一个布尔值，指定是否将粘贴的列表与周围的列表合并。 |
| [setSmartStyleBehavior(boolean value)](#setSmartStyleBehavior-boolean-) | 设置一个布尔值，指定样式在源文档和目标文档中具有相同名称时如何导入。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getForceCopyStyles() {#getForceCopyStyles--}
```
public boolean getForceCopyStyles()
```


获取一个布尔值，指示复制冲突的样式[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING)模式。默认值为 false 。

默认情况下，如果目标文档中已存在匹配样式，则源样式格式将展开为直接节点属性，并将该节点的样式重置为默认值。

当此选项设置为 true 时，源样式将被强制复制到具有唯一名称的目标文档中，并应用于导入的节点。

请注意，在这种情况下，不能保证目标文档中导入节点的格式将被保留。

**退货:**
 boolean - 一个布尔值，表示要复制冲突的样式[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING)模式。
### getIgnoreHeaderFooter() {#getIgnoreHeaderFooter--}
```
public boolean getIgnoreHeaderFooter()
```


获取一个布尔值，该值指定在以下情况下忽略页眉/页脚内容的源格式[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING)使用模式。默认值是true 。

**退货:**
布尔值 - 一个布尔值，指定如果出现以下情况则忽略页眉/页脚内容的源格式[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING)使用模式。
### getIgnoreTextBoxes() {#getIgnoreTextBoxes--}
```
public boolean getIgnoreTextBoxes()
```


获取一个布尔值，该值指定忽略文本框内容的源格式，如果[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING)使用模式。默认值是true 。

**退货:**
boolean - 一个布尔值，指定忽略文本框内容的源格式[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING)使用模式。
### getKeepSourceNumbering() {#getKeepSourceNumbering--}
```
public boolean getKeepSourceNumbering()
```


获取一个布尔值，该值指定编号在源文档和目标文档中发生冲突时将如何导入。默认值为 false 。

**退货:**
boolean - 一个布尔值，指定编号在源文档和目标文档中发生冲突时将如何导入。
### getMergePastedLists() {#getMergePastedLists--}
```
public boolean getMergePastedLists()
```


获取一个布尔值，该值指定粘贴的列表是否将与周围的列表合并。默认值为 false 。

**退货:**
boolean - 一个布尔值，指定粘贴的列表是否将与周围的列表合并。
### getSmartStyleBehavior() {#getSmartStyleBehavior--}
```
public boolean getSmartStyleBehavior()
```


获取一个布尔值，该值指定样式在源文档和目标文档中具有相同名称时将如何导入。默认值为 false 。

当这个选项是**enabled**，源样式将扩展为目标文档内的直接属性，如果[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING)使用导入模式。

当这个选项是**disabled**，源样式只有在编号时才会展开。不会覆盖现有目标属性，包括列表。

**退货:**
boolean - 一个布尔值，指定样式在源文档和目标文档中具有相同名称时将如何导入。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setForceCopyStyles(boolean value) {#setForceCopyStyles-boolean-}
```
public void setForceCopyStyles(boolean value)
```


设置一个布尔值，指示复制冲突的样式[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING)模式。默认值为 false 。

默认情况下，如果目标文档中已存在匹配样式，则源样式格式将展开为直接节点属性，并将该节点的样式重置为默认值。

当此选项设置为 true 时，源样式将被强制复制到具有唯一名称的目标文档中，并应用于导入的节点。

请注意，在这种情况下，不能保证目标文档中导入节点的格式将被保留。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，指示复制冲突的样式[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING)模式。 |

### setIgnoreHeaderFooter(boolean value) {#setIgnoreHeaderFooter-boolean-}
```
public void setIgnoreHeaderFooter(boolean value)
```


设置一个布尔值，指定在以下情况下忽略页眉/页脚内容的源格式[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING)使用模式。默认值是true 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，指定在以下情况下忽略页眉/页脚内容的源格式[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING)使用模式。 |

### setIgnoreTextBoxes(boolean value) {#setIgnoreTextBoxes-boolean-}
```
public void setIgnoreTextBoxes(boolean value)
```


设置一个布尔值，指定忽略文本框内容的源格式，如果[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING)使用模式。默认值是true 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，指定忽略文本框内容的源格式，如果[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING)使用模式。 |

### setKeepSourceNumbering(boolean value) {#setKeepSourceNumbering-boolean-}
```
public void setKeepSourceNumbering(boolean value)
```


设置一个布尔值，用于指定编号在源文档和目标文档中发生冲突时如何导入。默认值为 false 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，用于指定编号在源文档和目标文档中发生冲突时如何导入。 |

### setMergePastedLists(boolean value) {#setMergePastedLists-boolean-}
```
public void setMergePastedLists(boolean value)
```


设置一个布尔值，指定是否将粘贴的列表与周围的列表合并。默认值为 false 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，指定是否将粘贴的列表与周围的列表合并。 |

### setSmartStyleBehavior(boolean value) {#setSmartStyleBehavior-boolean-}
```
public void setSmartStyleBehavior(boolean value)
```


设置一个布尔值，指定样式在源文档和目标文档中具有相同名称时如何导入。默认值为 false 。

当这个选项是**enabled**，源样式将扩展为目标文档内的直接属性，如果[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING)使用导入模式。

当这个选项是**disabled**，源样式只有在编号时才会展开。不会覆盖现有目标属性，包括列表。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，指定在源文档和目标文档中具有相同名称时如何导入样式。 |

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
