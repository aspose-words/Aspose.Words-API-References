---
title: ControlChar
second_title: Aspose.Words for Java API 参考
description: 文档中经常遇到的控制字符。
type: docs
weight: 94
url: /zh/java/com.aspose.words/controlchar/
---

**遗产：**
java.lang.Object
```
public class ControlChar
```

文档中经常遇到的控制字符。

要了解更多信息，请访问**Working With Control Characters**文档文章。

提供相同常量的字符和字符串版本。例如：字符串 ControlChar.LineBreak 和 char ControlChar.LineBreakChar 具有相同的值。
## 字段

| 场地 | 描述 |
| --- | --- |
| [CELL](#CELL) | 表格单元格结束或表格行结束字符："\\x0007" 或 "\\一个”。 |
| [CELL_CHAR](#CELL-CHAR) | 表格单元格结尾或表格行结尾字符：(char)7 或 "\\一个”。 |
| [COLUMN_BREAK](#COLUMN-BREAK) | 列结束符："\\x000e”。 |
| [COLUMN_BREAK_CHAR](#COLUMN-BREAK-CHAR) | 列尾字符：(char)14。 |
| [CR](#CR) | 回车符："\\x000d" 或 "\\r"。 |
| [CR_LF](#CR-LF) | 回车后跟换行符："\\x000d\\x000a" 或 "\\r\\n”。 |
| [DEFAULT_TEXT_INPUT_CHAR](#DEFAULT-TEXT-INPUT-CHAR) | 这是在文本输入表单字段中用作默认值的“o”字符。 |
| [FIELD_END_CHAR](#FIELD-END-CHAR) | MS Word 字段字符的结尾：(char)21。 |
| [FIELD_SEPARATOR_CHAR](#FIELD-SEPARATOR-CHAR) | 字段分隔符将字段代码与字段值分开。 |
| [FIELD_START_CHAR](#FIELD-START-CHAR) | MS Word 字段字符的开头：(char)19。 |
| [LF](#LF) | 换行符："\\x000a" 或 "\\n”。 |
| [LINE_BREAK](#LINE-BREAK) | 换行符："\\x000b" 或 "\\v"。 |
| [LINE_BREAK_CHAR](#LINE-BREAK-CHAR) | 换行字符：(char)11 或 "\\v"。 |
| [LINE_FEED](#LINE-FEED) | 换行符："\\x000a" 或 "\\n”。 |
| [LINE_FEED_CHAR](#LINE-FEED-CHAR) | 换行字符：(char)10 或 "\\n”。 |
| [NON_BREAKING_HYPHEN_CHAR](#NON-BREAKING-HYPHEN-CHAR) | Microsoft Word 中的不间断连字符是 (char)30。 |
| [NON_BREAKING_SPACE](#NON-BREAKING-SPACE) | 不间断空格符："\\x00a0”。 |
| [NON_BREAKING_SPACE_CHAR](#NON-BREAKING-SPACE-CHAR) | 不间断空格字符：(char)160。 |
| [OPTIONAL_HYPHEN_CHAR](#OPTIONAL-HYPHEN-CHAR) | Microsoft Word 中的可选连字符是 (char)31。 |
| [PAGE_BREAK](#PAGE-BREAK) | 分页字符："\\x000c" 或 "\\F”。 |
| [PAGE_BREAK_CHAR](#PAGE-BREAK-CHAR) | 分页字符：(char)12 或 "\\F”。 |
| [PARAGRAPH_BREAK](#PARAGRAPH-BREAK) | 段尾字符："\\x000d" 或 "\\r"。 |
| [PARAGRAPH_BREAK_CHAR](#PARAGRAPH-BREAK-CHAR) | 段尾字符：(char)13 或 "\\r"。 |
| [SECTION_BREAK](#SECTION-BREAK) | 节尾字符："\\x000c" 或 "\\F”。 |
| [SECTION_BREAK_CHAR](#SECTION-BREAK-CHAR) | 节结束字符：(char)12 或 "\\F”。 |
| [SPACE_CHAR](#SPACE-CHAR) | 空格字符：(char)32。 |
| [TAB](#TAB) | 制表符："\\x0009" 或 "\\t"。 |
| [TAB_CHAR](#TAB-CHAR) | 制表符：(char)9 或 "\\t"。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### CELL {#CELL}
```
public static String CELL
```


表格单元格结束或表格行结束字符："\\x0007" 或 "\\一个”。

### CELL_CHAR {#CELL-CHAR}
```
public static char CELL_CHAR
```


表格单元格结尾或表格行结尾字符：(char)7 或 "\\一个”。

### COLUMN_BREAK {#COLUMN-BREAK}
```
public static String COLUMN_BREAK
```


列结束符："\\x000e”。

### COLUMN_BREAK_CHAR {#COLUMN-BREAK-CHAR}
```
public static char COLUMN_BREAK_CHAR
```


列尾字符：(char)14。

### CR {#CR}
```
public static String CR
```


回车符："\\x000d" 或 "\ \r". 同[PARAGRAPH\_BREAK](../../com.aspose.words/controlchar\#PARAGRAPH-BREAK).

### CR_LF {#CR-LF}
```
public static String CR_LF
```


回车后跟换行符："\\x000d\\x000a" 或 "\\r\\n"。在 Microsoft Word 文档中不这样使用，但通常在文本文件中用作分段符。

### DEFAULT_TEXT_INPUT_CHAR {#DEFAULT-TEXT-INPUT-CHAR}
```
public static char DEFAULT_TEXT_INPUT_CHAR
```


这是在文本输入表单字段中用作默认值的“o”字符。

### FIELD_END_CHAR {#FIELD-END-CHAR}
```
public static char FIELD_END_CHAR
```


MS Word 字段字符的结尾：(char)21。

### FIELD_SEPARATOR_CHAR {#FIELD-SEPARATOR-CHAR}
```
public static char FIELD_SEPARATOR_CHAR
```


字段分隔符将字段代码与字段值分开。在某些领域是可选的。值：（字符）20。

### FIELD_START_CHAR {#FIELD-START-CHAR}
```
public static char FIELD_START_CHAR
```


MS Word 字段字符的开头：(char)19。

### LF {#LF}
```
public static String LF
```


换行符："\\x000a" 或 "\ \n"。同[LINE\_FEED](../../com.aspose.words/controlchar\#LINE-FEED).

### LINE_BREAK {#LINE-BREAK}
```
public static String LINE_BREAK
```


换行符："\\x000b" 或 "\\v"。

### LINE_BREAK_CHAR {#LINE-BREAK-CHAR}
```
public static char LINE_BREAK_CHAR
```


换行字符：(char)11 或 "\\v"。

### LINE_FEED {#LINE-FEED}
```
public static String LINE_FEED
```


换行符："\\x000a" 或 "\ \n"。同[LF](../../com.aspose.words/controlchar\#LF).

### LINE_FEED_CHAR {#LINE-FEED-CHAR}
```
public static char LINE_FEED_CHAR
```


换行字符：(char)10 或 "\\n”。

### NON_BREAKING_HYPHEN_CHAR {#NON-BREAKING-HYPHEN-CHAR}
```
public static char NON_BREAKING_HYPHEN_CHAR
```


Microsoft Word 中的不间断连字符是 (char)30。

Microsoft Word 中的不间断连字符不对应于 Unicode 字符 U+2011 不间断连字符，而是表示告诉 Microsoft Word 显示连字符而不是换行的内部信息。

有用信息：http://www.cs.tut.fi/~jkorpela/dashes.html\#换行符。

### NON_BREAKING_SPACE {#NON-BREAKING-SPACE}
```
public static String NON_BREAKING_SPACE
```


不间断空格符："\\x00a0”。

### NON_BREAKING_SPACE_CHAR {#NON-BREAKING-SPACE-CHAR}
```
public static char NON_BREAKING_SPACE_CHAR
```


不间断空格字符：(char)160。

### OPTIONAL_HYPHEN_CHAR {#OPTIONAL-HYPHEN-CHAR}
```
public static char OPTIONAL_HYPHEN_CHAR
```


Microsoft Word 中的可选连字符是 (char)31。

Microsoft Word 中的可选连字符与 Unicode 字符 U+00AD 软连字符不对应。相反，它会插入告诉 Word 可能的断字点的内部信息。

### PAGE_BREAK {#PAGE-BREAK}
```
public static String PAGE_BREAK
```


分页字符："\\x000c" 或 "\ \f"。注意它的值与[SECTION\_BREAK](../../com.aspose.words/controlchar\#SECTION-BREAK).

### PAGE_BREAK_CHAR {#PAGE-BREAK-CHAR}
```
public static char PAGE_BREAK_CHAR
```


分页字符：(char)12 或 "\\F”。

### PARAGRAPH_BREAK {#PARAGRAPH-BREAK}
```
public static String PARAGRAPH_BREAK
```


段尾字符："\\x000d" 或 "\ \r". 同[CR](../../com.aspose.words/controlchar\#CR)

### PARAGRAPH_BREAK_CHAR {#PARAGRAPH-BREAK-CHAR}
```
public static char PARAGRAPH_BREAK_CHAR
```


段尾字符：(char)13 或 "\\r"。

### SECTION_BREAK {#SECTION-BREAK}
```
public static String SECTION_BREAK
```


节尾字符："\\x000c" 或 "\ \f"。注意它的值与[PAGE\_BREAK](../../com.aspose.words/controlchar\#PAGE-BREAK).

### SECTION_BREAK_CHAR {#SECTION-BREAK-CHAR}
```
public static char SECTION_BREAK_CHAR
```


节结束字符：(char)12 或 "\\F”。

### SPACE_CHAR {#SPACE-CHAR}
```
public static char SPACE_CHAR
```


空格字符：(char)32。

### TAB {#TAB}
```
public static String TAB
```


制表符："\\x0009" 或 "\\t"。

### TAB_CHAR {#TAB-CHAR}
```
public static char TAB_CHAR
```


制表符：(char)9 或 "\\t"。

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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
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
