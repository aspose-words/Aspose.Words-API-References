---
title: MailMergeCleanupOptions
second_title: Aspose.Words for Java API 参考
description:指定确定在邮件合并期间删除哪些项目的选项。
type: docs
weight: 381
url: /zh/java/com.aspose.words/mailmergecleanupoptions/
---

**遗产:**
java.lang.Object
```
public class MailMergeCleanupOptions
```

指定确定在邮件合并期间删除哪些项目的选项。
## 字段

| 字段 | 描述 |
| --- | --- |
| [NONE](#NONE) | 指定默认值。 |
| [REMOVE_CONTAINING_FIELDS](#REMOVE-CONTAINING-FIELDS) | 指定在删除嵌套合并字段时是否应从文档中删除包含合并字段（例如，IF）的字段。 |
| [REMOVE_EMPTY_PARAGRAPHS](#REMOVE-EMPTY-PARAGRAPHS) | 指定是否应从文档中删除包含没有数据的邮件合并字段的段落。 |
| [REMOVE_EMPTY_TABLE_ROWS](#REMOVE-EMPTY-TABLE-ROWS) | 指定是否应从文档中删除包含邮件合并区域的空行。 |
| [REMOVE_STATIC_FIELDS](#REMOVE-STATIC-FIELDS) | 指定是否应从文档中删除静态字段。 |
| [REMOVE_UNUSED_FIELDS](#REMOVE-UNUSED-FIELDS) | 指定是否应从文档中删除未使用的合并字段。 |
| [REMOVE_UNUSED_REGIONS](#REMOVE-UNUSED-REGIONS) | 指定是否应从文档中删除未使用的邮件合并区域。 |
| [length](#length) |  |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String mailMergeCleanupOptionsName)](#fromName-java.lang.String-) |  |
| [fromNames(Set mailMergeCleanupOptionsNames)](#fromNames-java.util.Set-) |  |
| [get班级()](#get班级--) |  |
| [getName(int mailMergeCleanupOptions)](#getName-int-) |  |
| [getNames(int mailMergeCleanupOptions)](#getNames-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int mailMergeCleanupOptions)](#toString-int-) |  |
| [toStringSet(int attr)](#toStringSet-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### NONE {#NONE}
```
public static int NONE
```


指定默认值。

### REMOVE_CONTAINING_FIELDS {#REMOVE-CONTAINING-FIELDS}
```
public static int REMOVE_CONTAINING_FIELDS
```


指定在删除嵌套合并字段时是否应从文档中删除包含合并字段（例如，IF）的字段。

### REMOVE_EMPTY_PARAGRAPHS {#REMOVE-EMPTY-PARAGRAPHS}
```
public static int REMOVE_EMPTY_PARAGRAPHS
```


指定是否应从文档中删除包含没有数据的邮件合并字段的段落。设置此选项时，包含区域开始和结束合并字段的段落也会被删除，否则这些字段为空。

### REMOVE_EMPTY_TABLE_ROWS {#REMOVE-EMPTY-TABLE-ROWS}
```
public static int REMOVE_EMPTY_TABLE_ROWS
```


指定是否应从文档中删除包含邮件合并区域的空行。此选项仅适用于与区域的邮件合并。

### REMOVE_STATIC_FIELDS {#REMOVE-STATIC-FIELDS}
```
public static int REMOVE_STATIC_FIELDS
```


指定是否应从文档中删除静态字段。静态字段是字段，其结果在任何文档更改时保持不变。字段，它们不会将结果存储在文档中，而是动态计算的（例如[字段类型.FIELD\_LIST\_NUM](../../com.aspose.words/fieldtype\#FIELD-LIST-NUM), [字段类型.FIELD\_SYMBOL](../../com.aspose.words/fieldtype\#FIELD-SYMBOL)等）不被认为是静态的。以下是字段类型的完整列表，它们不被认为是静态的：

 *  [字段类型.FIELD\_ADVANCE](../../com.aspose.words/fieldtype\#FIELD-ADVANCE)
 *  [字段类型.FIELD\_AUTO\_NUM](../../com.aspose.words/fieldtype\#FIELD-AUTO-NUM)
 *  [字段类型.FIELD\_AUTO\_NUM\_LEGAL](../../com.aspose.words/fieldtype\#FIELD-AUTO-NUM-LEGAL)
 *  [字段类型.FIELD\_AUTO\_NUM\_OUTLINE](../../com.aspose.words/fieldtype\#FIELD-AUTO-NUM-OUTLINE)
 *  [字段类型.FIELD\_BARCODE](../../com.aspose.words/fieldtype\#FIELD-BARCODE)
 *  [字段类型.FIELD\_BIDI\_OUTLINE](../../com.aspose.words/fieldtype\#FIELD-BIDI-OUTLINE)
 *  [字段类型.FIELD\_DATE](../../com.aspose.words/fieldtype\#FIELD-DATE)
 *  [字段类型.FIELD\_DISPLAY\_BARCODE](../../com.aspose.words/fieldtype\#FIELD-DISPLAY-BARCODE)
 *  [字段类型.FIELD\_MERGE\_BARCODE](../../com.aspose.words/fieldtype\#FIELD-MERGE-BARCODE)
 *  [字段类型.FIELD\_FORM\_CHECK\_BOX](../../com.aspose.words/fieldtype\#FIELD-FORM-CHECK-BOX)
 *  [字段类型.FIELD\_FORM\_DROP\_DOWN](../../com.aspose.words/fieldtype\#FIELD-FORM-DROP-DOWN)
 *  [字段类型.FIELD\_FORMULA](../../com.aspose.words/fieldtype\#FIELD-FORMULA)
 *  [字段类型.FIELD\_GO\_TO\_BUTTON](../../com.aspose.words/fieldtype\#FIELD-GO-TO-BUTTON)
 *  [字段类型.FIELD\_HYPERLINK](../../com.aspose.words/fieldtype\#FIELD-HYPERLINK)
 *  [字段类型.FIELD\_INCLUDE\_TEXT](../../com.aspose.words/fieldtype\#FIELD-INCLUDE-TEXT)
 *  [字段类型.FIELD\_INDEX\_ENTRY](../../com.aspose.words/fieldtype\#FIELD-INDEX-ENTRY)
 *  [字段类型.FIELD\_LINK](../../com.aspose.words/fieldtype\#FIELD-LINK)
 *  [字段类型.FIELD\_LIST\_NUM](../../com.aspose.words/fieldtype\#FIELD-LIST-NUM)
 *  [字段类型.FIELD\_MACRO\_BUTTON](../../com.aspose.words/fieldtype\#FIELD-MACRO-BUTTON)
 *  [字段类型.FIELD\_NOTE\_REF](../../com.aspose.words/fieldtype\#FIELD-NOTE-REF)
 *  [字段类型.FIELD\_NUM\_PAGES](../../com.aspose.words/fieldtype\#FIELD-NUM-PAGES)
 *  [字段类型.FIELD\_PAGE](../../com.aspose.words/fieldtype\#FIELD-PAGE)
 *  [字段类型.FIELD\_PAGE\_REF](../../com.aspose.words/fieldtype\#FIELD-PAGE-REF)
 *  [字段类型.FIELD\_PRINT](../../com.aspose.words/fieldtype\#FIELD-PRINT)
 *  [字段类型.FIELD\_PRINT\_DATE](../../com.aspose.words/fieldtype\#FIELD-PRINT-DATE)
 *  [字段类型.FIELD\_PRIVATE](../../com.aspose.words/fieldtype\#FIELD-PRIVATE)
 *  [字段类型.FIELD\_REF\_DOC](../../com.aspose.words/fieldtype\#FIELD-REF-DOC)
 *  [字段类型.FIELD\_SECTION](../../com.aspose.words/fieldtype\#FIELD-SECTION)
 *  [字段类型.FIELD\_SECTION\_PAGES](../../com.aspose.words/fieldtype\#FIELD-SECTION-PAGES)
 *  [字段类型.FIELD\_SYMBOL](../../com.aspose.words/fieldtype\#FIELD-SYMBOL)
 *  [字段类型.FIELD\_TIME](../../com.aspose.words/fieldtype\#FIELD-TIME)
 *  [字段类型.FIELD\_TOA\_ENTRY](../../com.aspose.words/fieldtype\#FIELD-TOA-ENTRY)
 *  [字段类型.FIELD\_TOC\_ENTRY](../../com.aspose.words/fieldtype\#FIELD-TOC-ENTRY)

### REMOVE_UNUSED_FIELDS {#REMOVE-UNUSED-FIELDS}
```
public static int REMOVE_UNUSED_FIELDS
```


指定是否应从文档中删除未使用的合并字段。

### REMOVE_UNUSED_REGIONS {#REMOVE-UNUSED-REGIONS}
```
public static int REMOVE_UNUSED_REGIONS
```


指定是否应从文档中删除未使用的邮件合并区域。此选项仅适用于与区域的邮件合并。

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
### fromName(String mailMergeCleanupOptionsName) {#fromName-java.lang.String-}
```
public static int fromName(String mailMergeCleanupOptionsName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| mailMergeCleanupOptionsName | java.lang.String |  |

**退货:**
整数
### fromNames(Set mailMergeCleanupOptionsNames) {#fromNames-java.util.Set-}
```
public static int fromNames(Set mailMergeCleanupOptionsNames)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| mailMergeCleanupOptionsNames | java.util.Set |  |

**退货:**
整数
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getName(int mailMergeCleanupOptions) {#getName-int-}
```
public static String getName(int mailMergeCleanupOptions)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| mailMergeCleanupOptions | int |  |

**退货:**
java.lang.String
### getNames(int mailMergeCleanupOptions) {#getNames-int-}
```
public static Set getNames(int mailMergeCleanupOptions)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| mailMergeCleanupOptions | int |  |

**退货:**
java.util.Set
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
### toString(int mailMergeCleanupOptions) {#toString-int-}
```
public static String toString(int mailMergeCleanupOptions)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| mailMergeCleanupOptions | int |  |

**退货:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int-}
```
public static String toStringSet(int attr)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| attr | int |  |

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
