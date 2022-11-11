---
title: ImportFormatMode
second_title: Aspose.Words for Java API 参考
description:指定从另一个文档导入内容时如何合并格式。
type: docs
weight: 346
url: /zh/java/com.aspose.words/importformatmode/
---

**遗产:**
java.lang.Object
```
public class ImportFormatMode
```

指定从另一个文档导入内容时如何合并格式。

当您将节点从一个文档复制到另一个文档时，此选项指定当两个文档具有相同名称但格式不同的样式时如何解析格式。

格式解析如下：

1.  内置样式使用与区域设置无关的样式标识符进行匹配。用户定义的样式使用区分大小写的样式名称进行匹配。
2.  如果在目标文档中找不到匹配的样式，则将该样式（及其引用的所有样式）复制到目标文档中，并更新导入的节点以引用新样式。
3.  如果目标文档中已经存在匹配的样式，会发生什么取决于传递给的 importFormatMode 参数**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**如下所述。

使用时**UseDestinationStyles**选项，如果目标文档中已存在匹配样式，则不会复制该样式，并且会更新导入的节点以引用现有样式。

使用的缺点**UseDestinationStyles**是与源文档相比，导入的文本在目标文档中可能看起来不同。例如，源文档中的“标题 1”样式使用 Arial 16pt 字体，而目标文档中的“标题 1”样式使用 Times New Roman 14pt 字体。当导入没有其他直接格式的“标题 1”样式的文本时，它将在目标文档中显示为 Times New Roman 14pt 字体。

**KeepSourceFormatting**选项允许确保导入的内容在目标文档中看起来与在源文档中的外观相同。如果目标文档中已存在匹配样式，则源样式格式将扩展为直接节点属性，并将样式更改为正常。如果目标文档中不存在该样式，则将源样式导入目标文档并应用于导入的节点。请注意，即使源样式不存在于目标文档中，也不总是可以保留它。在这种情况下，这种样式的格式将扩展为直接节点属性，以支持保留原始节点格式。

使用的缺点**KeepSourceFormatting**就是如果您执行多个导入，您最终可能会在目标文档中使用许多样式，这可能会使在 Microsoft Word 中使用一致的样式格式对于该文档来说很困难。

使用**KeepDifferentStyles**如果它们提供的格式与源文档中的样式相同，则选项允许重用目标样式。如果目标文档中的样式与源文档中的样式不同，则将其导入。

**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**
## 字段

| 字段 | 描述 |
| --- | --- |
| [KEEP_DIFFERENT_STYLES](#KEEP-DIFFERENT-STYLES) | 仅复制与源文档中的样式不同的样式。 |
| [KEEP_SOURCE_FORMATTING](#KEEP-SOURCE-FORMATTING) | 将所有需要的样式复制到目标文档，如果需要，生成唯一的样式名称。 |
| [USE_DESTINATION_STYLES](#USE-DESTINATION-STYLES) | 使用目标文档样式并复制新样式。 |
| [length](#length) |  |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String importFormatModeName)](#fromName-java.lang.String-) |  |
| [get班级()](#get班级--) |  |
| [getName(int importFormatMode)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int importFormatMode)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### KEEP_DIFFERENT_STYLES {#KEEP-DIFFERENT-STYLES}
```
public static int KEEP_DIFFERENT_STYLES
```


仅复制与源文档中的样式不同的样式。

### KEEP_SOURCE_FORMATTING {#KEEP-SOURCE-FORMATTING}
```
public static int KEEP_SOURCE_FORMATTING
```


将所有需要的样式复制到目标文档，如果需要，生成唯一的样式名称。

### USE_DESTINATION_STYLES {#USE-DESTINATION-STYLES}
```
public static int USE_DESTINATION_STYLES
```


使用目标文档样式并复制新样式。这是默认选项。

### length {#length}
```
public static int length
```


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
### fromName(String importFormatModeName) {#fromName-java.lang.String-}
```
public static int fromName(String importFormatModeName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| importFormatModeName | java.lang.String |  |

**退货:**
整数
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getName(int importFormatMode) {#getName-int-}
```
public static String getName(int importFormatMode)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| importFormatMode | int |  |

**退货:**
java.lang.String
### getValues() {#getValues--}
```
public static int[] getValues()
```




**退货:**
整数[]
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




### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### toString(int importFormatMode) {#toString-int-}
```
public static String toString(int importFormatMode)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| importFormatMode | int |  |

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
