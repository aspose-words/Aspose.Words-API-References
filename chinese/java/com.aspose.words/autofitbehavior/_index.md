---
title: AutoFitBehavior
second_title: Aspose.Words for Java API 参考
description: 确定当您调用 MAspose.Words.Tables.Table.AutoFitAspose.Words.Tables.AutoFitBehavior 方法时 Aspose.Words 如何调整表格的大小。
type: docs
weight: 15
url: /zh/java/com.aspose.words/autofitbehavior/
---

**遗产:**
java.lang.Object
```
public class AutoFitBehavior
```

确定 Aspose.Words 在您调用**M:Aspose.Words.Tables.Table.AutoFit(Aspose.Words.Tables.AutoFitBehavior)**方法。
## 字段

| 场地 | 描述 |
| --- | --- |
| [AUTO_FIT_TO_CONTENTS](#AUTO-FIT-TO-CONTENTS) | Aspose.Words 启用 AutoFit 选项，从表格和所有单元格中删除首选宽度，然后更新表格布局。 |
| [AUTO_FIT_TO_WINDOW](#AUTO-FIT-TO-WINDOW) | 当您使用此值时，Aspose.Words 启用 AutoFit 选项，将表格的首选宽度设置为 100%，从所有单元格中删除首选宽度，然后更新表格布局。 |
| [FIXED_COLUMN_WIDTHS](#FIXED-COLUMN-WIDTHS) | Aspose.Words 禁用 AutoFit 选项并从表中删除首选。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String autoFitBehaviorName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int autoFitBehavior)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int autoFitBehavior)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### AUTO_FIT_TO_CONTENTS {#AUTO-FIT-TO-CONTENTS}
```
public static int AUTO_FIT_TO_CONTENTS
```


Aspose.Words 启用 AutoFit 选项，从表格和所有单元格中删除首选宽度，然后更新表格布局。

在生成的表格中，单元格宽度会更新以适合表格内容。最有可能的是，表格会缩小。

### AUTO_FIT_TO_WINDOW {#AUTO-FIT-TO-WINDOW}
```
public static int AUTO_FIT_TO_WINDOW
```


当您使用此值时，Aspose.Words 启用 AutoFit 选项，将表格的首选宽度设置为 100%，从所有单元格中删除首选宽度，然后更新表格布局。

结果，表格占据了所有可用宽度，并且单元格宽度被更新以适应表格内容。

### FIXED_COLUMN_WIDTHS {#FIXED-COLUMN-WIDTHS}
```
public static int FIXED_COLUMN_WIDTHS
```


Aspose.Words 禁用 AutoFit 选项并从表中删除首选。

单元格的宽度保持不变，因为它们由它们指定[CellFormat.getWidth()](../../com.aspose.words/cellformat\#getWidth--) / [CellFormat.setWidth(double)](../../com.aspose.words/cellformat\#setWidth-double-)特性。

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
### fromName(String autoFitBehaviorName) {#fromName-java.lang.String-}
```
public static int fromName(String autoFitBehaviorName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| autoFitBehaviorName | java.lang.String |  |

**退货:**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getName(int autoFitBehavior) {#getName-int-}
```
public static String getName(int autoFitBehavior)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| autoFitBehavior | int |  |

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
### toString(int autoFitBehavior) {#toString-int-}
```
public static String toString(int autoFitBehavior)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| autoFitBehavior | int |  |

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
