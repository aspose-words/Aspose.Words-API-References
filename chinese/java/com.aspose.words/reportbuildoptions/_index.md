---
title: ReportBuildOptions
second_title: Aspose.Words for Java API 参考
description: 指定构建报告时控制行为的选项。
type: docs
weight: 477
url: /zh/java/com.aspose.words/reportbuildoptions/
---

**遗产:**
java.lang.Object
```
public class ReportBuildOptions
```

指定控制行为的选项[ReportingEngine](../../com.aspose.words/reportingengine)在构建报告时。
## 字段

| 场地 | 描述 |
| --- | --- |
| [ALLOW_MISSING_MEMBERS](#ALLOW-MISSING-MEMBERS) | 指定缺少的对象成员应被引擎视为空文字。 |
| [INLINE_ERROR_MESSAGES](#INLINE-ERROR-MESSAGES) | 指定引擎应将模板语法错误消息内联到输出文档中。 |
| [NONE](#NONE) | 指定默认选项。 |
| [REMOVE_EMPTY_PARAGRAPHS](#REMOVE-EMPTY-PARAGRAPHS) | 指定引擎应删除在模板语法标记被删除或替换为空值后变为空的段落。 |
| [RESPECT_JPEG_EXIF_ORIENTATION](#RESPECT-JPEG-EXIF-ORIENTATION) | 指定引擎应使用 EXIF\\u200b\\u200bimage 方向值以适当地旋转插入的 JPEG 图像。 |
| [USE_LEGACY_HEADER_FOOTER_VISITING](#USE-LEGACY-HEADER-FOOTER-VISITING) | 指定引擎应该按照与 Aspose.Words 21.9 之前的版本兼容的顺序访问部分子节点（页眉、页脚、正文）。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String reportBuildOptionsName)](#fromName-java.lang.String-) |  |
| [fromNames(Set reportBuildOptionsNames)](#fromNames-java.util.Set-) |  |
| [getClass()](#getClass--) |  |
| [getName(int reportBuildOptions)](#getName-int-) |  |
| [getNames(int reportBuildOptions)](#getNames-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int reportBuildOptions)](#toString-int-) |  |
| [toStringSet(int attr)](#toStringSet-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ALLOW_MISSING_MEMBERS {#ALLOW-MISSING-MEMBERS}
```
public static int ALLOW_MISSING_MEMBERS
```


指定缺少的对象成员应被引擎视为空文字。此选项仅影响对实例（即非静态）对象成员和扩展方法的访问。如果未设置此选项，则引擎在遇到缺少的对象成员时会引发异常。

### INLINE_ERROR_MESSAGES {#INLINE-ERROR-MESSAGES}
```
public static int INLINE_ERROR_MESSAGES
```


指定引擎应将模板语法错误消息内联到输出文档中。如果未设置此选项，则引擎在遇到语法错误时会抛出异常。

### NONE {#NONE}
```
public static int NONE
```


指定默认选项。

### REMOVE_EMPTY_PARAGRAPHS {#REMOVE-EMPTY-PARAGRAPHS}
```
public static int REMOVE_EMPTY_PARAGRAPHS
```


指定引擎应删除在模板语法标记被删除或替换为空值后变为空的段落。

### RESPECT_JPEG_EXIF_ORIENTATION {#RESPECT-JPEG-EXIF-ORIENTATION}
```
public static int RESPECT_JPEG_EXIF_ORIENTATION
```


指定引擎应使用 EXIF\\u200b\\u200bimage 方向值以适当地旋转插入的 JPEG 图像。

### USE_LEGACY_HEADER_FOOTER_VISITING {#USE-LEGACY-HEADER-FOOTER-VISITING}
```
public static int USE_LEGACY_HEADER_FOOTER_VISITING
```


指定引擎应该按照与 Aspose.Words 21.9 之前的版本兼容的顺序访问部分子节点（页眉、页脚、正文）。

默认情况下，引擎将页眉和页脚视为链接到分节符。也就是说，当访问 section 子节点时，首先访问 body，然后才访问页眉和页脚。这与 Microsoft Word 在复制粘贴或删除多节内容时的行为一致，并在大多数情况下产生更正确的结果。

在 Aspose.Words 21.9 之前，引擎使用另一种访问顺序：Section 子节点按照它们在文档中出现的顺序被访问。将此值应用于[ReportingEngine.getOptions()](../../com.aspose.words/reportingengine\#getOptions--) / [ReportingEngine.setOptions(int)](../../com.aspose.words/reportingengine\#setOptions-int-)如果需要与旧版本的 Aspose.Words 兼容。

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
### fromName(String reportBuildOptionsName) {#fromName-java.lang.String-}
```
public static int fromName(String reportBuildOptionsName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| reportBuildOptionsName | java.lang.String |  |

**退货:**
整数
### fromNames(Set reportBuildOptionsNames) {#fromNames-java.util.Set-}
```
public static int fromNames(Set reportBuildOptionsNames)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| reportBuildOptionsNames | java.util.Set |  |

**退货:**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getName(int reportBuildOptions) {#getName-int-}
```
public static String getName(int reportBuildOptions)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| reportBuildOptions | int |  |

**退货:**
java.lang.String
### getNames(int reportBuildOptions) {#getNames-int-}
```
public static Set getNames(int reportBuildOptions)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| reportBuildOptions | int |  |

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
### toString(int reportBuildOptions) {#toString-int-}
```
public static String toString(int reportBuildOptions)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| reportBuildOptions | int |  |

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
