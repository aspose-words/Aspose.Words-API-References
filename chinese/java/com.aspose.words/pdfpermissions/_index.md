---
title: PdfPermissions
second_title: Aspose.Words for Java API Reference
description: 指定允许用户对加密的 PDF 文档进行的操作。
type: docs
weight: 460
url: /zh/java/com.aspose.words/pdfpermissions/
---

**遗产:**
java.lang.Object
```
public class PdfPermissions
```

指定允许用户对加密的 PDF 文档进行的操作。
## 字段

| 字段 | 描述 |
| --- | --- |
| [ALLOW_ALL](#ALLOW-ALL) | 允许对 PDF 文档进行所有操作。 |
| [CONTENT_COPY](#CONTENT-COPY) | 通过非受控者控制的操作复制或以其他方式从文档中提取文本和图形[CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions\#CONTENT-COPY-FOR-ACCESSIBILITY). |
| [CONTENT_COPY_FOR_ACCESSIBILITY](#CONTENT-COPY-FOR-ACCESSIBILITY) | 提取文本和图形（以支持残障用户的可访问性或用于其他目的）。 |
| [DISALLOW_ALL](#DISALLOW-ALL) | 禁止对 PDF 文档进行所有操作。 |
| [DOCUMENT_ASSEMBLY](#DOCUMENT-ASSEMBLY) | 组装文档（插入、旋转或删除页面并创建文档大纲项目或缩略图），即使[MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions\#MODIFY-CONTENTS)清楚了。 |
| [FILL_IN](#FILL-IN) | 填写现有的交互式表单域（包括签名域），即使[MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions\#MODIFY-CONTENTS)清楚了。 |
| [HIGH_RESOLUTION_PRINTING](#HIGH-RESOLUTION-PRINTING) | 根据实现相关的算法，将文档打印为可以生成 PDF 内容的忠实数字副本的表示形式。 |
| [MODIFY_ANNOTATIONS](#MODIFY-ANNOTATIONS) | 添加或修改文本注释，填写交互式表单字段，以及，如果[MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions\#MODIFY-CONTENTS)还可以设置、创建或修改交互式表单字段（包括签名字段）。 |
| [MODIFY_CONTENTS](#MODIFY-CONTENTS) | 通过非受控者控制的操作修改文档内容[MODIFY\_ANNOTATIONS](../../com.aspose.words/pdfpermissions\#MODIFY-ANNOTATIONS), [FILL\_IN](../../com.aspose.words/pdfpermissions\#FILL-IN)， 和[DOCUMENT\_ASSEMBLY](../../com.aspose.words/pdfpermissions\#DOCUMENT-ASSEMBLY). |
| [PRINTING](#PRINTING) | 打印文档（可能不是最高质量级别，取决于是否[HIGH\_RESOLUTION\_PRINTING](../../com.aspose.words/pdfpermissions\#HIGH-RESOLUTION-PRINTING)也设置）。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String pdfPermissionsName)](#fromName-java.lang.String-) |  |
| [fromNames(Set pdfPermissionsNames)](#fromNames-java.util.Set-) |  |
| [get班级()](#get班级--) |  |
| [getName(int pdfPermissions)](#getName-int-) |  |
| [getNames(int pdfPermissions)](#getNames-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int pdfPermissions)](#toString-int-) |  |
| [toStringSet(int attr)](#toStringSet-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ALLOW_ALL {#ALLOW-ALL}
```
public static int ALLOW_ALL
```


允许对 PDF 文档进行所有操作。

### CONTENT_COPY {#CONTENT-COPY}
```
public static int CONTENT_COPY
```


通过非受控者控制的操作复制或以其他方式从文档中提取文本和图形[CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions\#CONTENT-COPY-FOR-ACCESSIBILITY).

### CONTENT_COPY_FOR_ACCESSIBILITY {#CONTENT-COPY-FOR-ACCESSIBILITY}
```
public static int CONTENT_COPY_FOR_ACCESSIBILITY
```


提取文本和图形（以支持残障用户的可访问性或用于其他目的）。

### DISALLOW_ALL {#DISALLOW-ALL}
```
public static int DISALLOW_ALL
```


禁止对 PDF 文档进行所有操作。这是默认值。

### DOCUMENT_ASSEMBLY {#DOCUMENT-ASSEMBLY}
```
public static int DOCUMENT_ASSEMBLY
```


组装文档（插入、旋转或删除页面并创建文档大纲项目或缩略图），即使[MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions\#MODIFY-CONTENTS)清楚了。

### FILL_IN {#FILL-IN}
```
public static int FILL_IN
```


填写现有的交互式表单域（包括签名域），即使[MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions\#MODIFY-CONTENTS)清楚了。

### HIGH_RESOLUTION_PRINTING {#HIGH-RESOLUTION-PRINTING}
```
public static int HIGH_RESOLUTION_PRINTING
```


根据实现相关的算法，将文档打印为可以生成 PDF 内容的忠实数字副本的表示形式。当这个标志被清除时（并且[PRINTING](../../com.aspose.words/pdfpermissions\#PRINTING)已设置），打印应限于外观的低级表示，可能质量下降。

### MODIFY_ANNOTATIONS {#MODIFY-ANNOTATIONS}
```
public static int MODIFY_ANNOTATIONS
```


添加或修改文本注释，填写交互式表单字段，以及，如果[MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions\#MODIFY-CONTENTS)还可以设置、创建或修改交互式表单字段（包括签名字段）。

### MODIFY_CONTENTS {#MODIFY-CONTENTS}
```
public static int MODIFY_CONTENTS
```


通过非受控者控制的操作修改文档内容[MODIFY\_ANNOTATIONS](../../com.aspose.words/pdfpermissions\#MODIFY-ANNOTATIONS), [FILL\_IN](../../com.aspose.words/pdfpermissions\#FILL-IN)， 和[DOCUMENT\_ASSEMBLY](../../com.aspose.words/pdfpermissions\#DOCUMENT-ASSEMBLY).

### PRINTING {#PRINTING}
```
public static int PRINTING
```


打印文档（可能不是最高质量级别，取决于是否[HIGH\_RESOLUTION\_PRINTING](../../com.aspose.words/pdfpermissions\#HIGH-RESOLUTION-PRINTING)也设置）。

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
### fromName(String pdfPermissionsName) {#fromName-java.lang.String-}
```
public static int fromName(String pdfPermissionsName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pdfPermissionsName | java.lang.String |  |

**退货:**
整数
### fromNames(Set pdfPermissionsNames) {#fromNames-java.util.Set-}
```
public static int fromNames(Set pdfPermissionsNames)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pdfPermissionsNames | java.util.Set |  |

**退货:**
整数
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getName(int pdfPermissions) {#getName-int-}
```
public static String getName(int pdfPermissions)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pdfPermissions | int |  |

**退货:**
java.lang.String
### getNames(int pdfPermissions) {#getNames-int-}
```
public static Set getNames(int pdfPermissions)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pdfPermissions | int |  |

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
### toString(int pdfPermissions) {#toString-int-}
```
public static String toString(int pdfPermissions)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pdfPermissions | int |  |

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
