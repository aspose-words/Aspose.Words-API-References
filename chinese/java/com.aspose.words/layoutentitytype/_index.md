---
title: LayoutEntityType
second_title: Aspose.Words for Java API 参考
description: 布局实体的类型。
type: docs
weight: 359
url: /zh/java/com.aspose.words/layoutentitytype/
---

**遗产：**
java.lang.Object
```
public class LayoutEntityType
```

布局实体的类型。
## 字段

| 场地 | 描述 |
| --- | --- |
| [CELL](#CELL) | 代表一个表格单元格。 |
| [COLUMN](#COLUMN) | 表示页面上的一列文本。 |
| [COMMENT](#COMMENT) | 表示评论内容的占位符。 |
| [ENDNOTE](#ENDNOTE) | 表示尾注内容的占位符。 |
| [FOOTNOTE](#FOOTNOTE) | 表示脚注内容的占位符。 |
| [HEADER_FOOTER](#HEADER-FOOTER) | 表示页面上页眉/页脚内容的占位符。 |
| [LINE](#LINE) | 表示文本和内联对象的字符行。 |
| [NONE](#NONE) | 默认值。 |
| [NOTE](#NOTE) | 代表笔记内容的占位符。 |
| [NOTE_SEPARATOR](#NOTE-SEPARATOR) | 表示脚注/尾注分隔符。 |
| [PAGE](#PAGE) | 表示文档的页面。 |
| [ROW](#ROW) | 代表表格行。 |
| [SPAN](#SPAN) | 表示一行中的一个或多个字符。 |
| [TEXT_BOX](#TEXT-BOX) | 表示形状内的文本区域。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String layoutEntityTypeName)](#fromName-java.lang.String-) |  |
| [fromNames(Set layoutEntityTypeNames)](#fromNames-java.util.Set-) |  |
| [getClass()](#getClass--) |  |
| [getName(int layoutEntityType)](#getName-int-) |  |
| [getNames(int layoutEntityType)](#getNames-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int layoutEntityType)](#toString-int-) |  |
| [toStringSet(int attr)](#toStringSet-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### CELL {#CELL}
```
public static int CELL
```


代表一个表格单元格。细胞可能有[LINE](../../com.aspose.words/layoutentitytype\#LINE)和[ROW](../../com.aspose.words/layoutentitytype\#ROW)子实体。

### COLUMN {#COLUMN}
```
public static int COLUMN
```


表示页面上的一列文本。列可能具有与以下相同的子实体[CELL](../../com.aspose.words/layoutentitytype\#CELL) 加上[FOOTNOTE](../../com.aspose.words/layoutentitytype\#FOOTNOTE), [ENDNOTE](../../com.aspose.words/layoutentitytype\#ENDNOTE)和[NOTE\_SEPARATOR](../../com.aspose.words/layoutentitytype\#NOTE-SEPARATOR)实体。

### COMMENT {#COMMENT}
```
public static int COMMENT
```


表示评论内容的占位符。评论可能有[LINE](../../com.aspose.words/layoutentitytype\#LINE)和[ROW](../../com.aspose.words/layoutentitytype\#ROW)子实体。

### ENDNOTE {#ENDNOTE}
```
public static int ENDNOTE
```


表示尾注内容的占位符。尾注可能有[NOTE](../../com.aspose.words/layoutentitytype\#NOTE)子实体。

### FOOTNOTE {#FOOTNOTE}
```
public static int FOOTNOTE
```


表示脚注内容的占位符。脚注可能有[NOTE](../../com.aspose.words/layoutentitytype\#NOTE)子实体。

### HEADER_FOOTER {#HEADER-FOOTER}
```
public static int HEADER_FOOTER
```


表示页面上页眉/页脚内容的占位符。 HeaderFooter 可能有[LINE](../../com.aspose.words/layoutentitytype\#LINE)和[ROW](../../com.aspose.words/layoutentitytype\#ROW)子实体。

### LINE {#LINE}
```
public static int LINE
```


表示文本和内联对象的字符行。线路可能有[SPAN](../../com.aspose.words/layoutentitytype\#SPAN)子实体。

### NONE {#NONE}
```
public static int NONE
```


默认值。

### NOTE {#NOTE}
```
public static int NOTE
```


代表笔记内容的占位符。注意可能有[LINE](../../com.aspose.words/layoutentitytype\#LINE)和[ROW](../../com.aspose.words/layoutentitytype\#ROW)子实体。

### NOTE_SEPARATOR {#NOTE-SEPARATOR}
```
public static int NOTE_SEPARATOR
```


表示脚注/尾注分隔符。注意分隔符可能有[LINE](../../com.aspose.words/layoutentitytype\#LINE)和[ROW](../../com.aspose.words/layoutentitytype\#ROW)子实体。

### PAGE {#PAGE}
```
public static int PAGE
```


表示文档的页面。页面可能有[COLUMN](../../com.aspose.words/layoutentitytype\#COLUMN), [HEADER\_FOOTER](../../com.aspose.words/layoutentitytype\#HEADER-FOOTER)和[COMMENT](../../com.aspose.words/layoutentitytype\#COMMENT)子实体。

### ROW {#ROW}
```
public static int ROW
```


代表表格行。行可能有[CELL](../../com.aspose.words/layoutentitytype\#CELL)作为子实体。

### SPAN {#SPAN}
```
public static int SPAN
```


表示一行中的一个或多个字符。这包括特殊字符，如字段开始/结束标记、书签和注释。 Span 可能没有子实体。

### TEXT_BOX {#TEXT-BOX}
```
public static int TEXT_BOX
```


表示形状内的文本区域。文本框可能有[LINE](../../com.aspose.words/layoutentitytype\#LINE)和[ROW](../../com.aspose.words/layoutentitytype\#ROW)子实体。

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货：**
布尔值
### fromName(String layoutEntityTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String layoutEntityTypeName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| layoutEntityTypeName | java.lang.String |  |

**退货：**
整数
### fromNames(Set layoutEntityTypeNames) {#fromNames-java.util.Set-}
```
public static int fromNames(Set layoutEntityTypeNames)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| layoutEntityTypeNames | java.util.Set |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int layoutEntityType) {#getName-int-}
```
public static String getName(int layoutEntityType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| layoutEntityType | int |  |

**退货：**
java.lang.字符串
### getNames(int layoutEntityType) {#getNames-int-}
```
public static Set getNames(int layoutEntityType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| layoutEntityType | int |  |

**退货：**
java.util.Set
### getValues() {#getValues--}
```
public static int[] getValues()
```




**退货：**
整数[]
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
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




**退货：**
java.lang.字符串
### toString(int layoutEntityType) {#toString-int-}
```
public static String toString(int layoutEntityType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| layoutEntityType | int |  |

**退货：**
java.lang.字符串
### toStringSet(int attr) {#toStringSet-int-}
```
public static String toStringSet(int attr)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| attr | int |  |

**退货：**
java.lang.字符串
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
