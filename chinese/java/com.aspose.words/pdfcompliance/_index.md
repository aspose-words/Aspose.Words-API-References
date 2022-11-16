---
title: PdfCompliance
second_title: Aspose.Words for Java API 参考
description: 指定 PDF 标准合规级别。
type: docs
weight: 449
url: /zh/java/com.aspose.words/pdfcompliance/
---

**遗产：**
java.lang.Object
```
public class PdfCompliance
```

指定 PDF 标准合规级别。
## 字段

| 场地 | 描述 |
| --- | --- |
| [PDF_17](#PDF-17) | 输出文件将符合 PDF 1.7 (ISO 32000-1) 标准。 |
| [PDF_20](#PDF-20) | 输出文件将符合 PDF 2.0 (ISO 32000-2) 标准。 |
| [PDF_A_1_A](#PDF-A-1-A) | 输出文件将符合 PDF/A-1a (ISO 19005-1) 标准。 |
| [PDF_A_1_B](#PDF-A-1-B) | 输出文件将符合 PDF/A-1b (ISO 19005-1) 标准。 |
| [PDF_A_2_A](#PDF-A-2-A) | 输出文件将符合 PDF/A-2a (ISO 19005-2) 标准。 |
| [PDF_A_2_U](#PDF-A-2-U) | 输出文件将符合 PDF/A-2u (ISO 19005-2) 标准。 |
| [PDF_A_4](#PDF-A-4) | 输出文件将符合 PDF/A-4 (ISO 19005-4:2020) 标准。 |
| [PDF_UA_1](#PDF-UA-1) | 输出文件将符合 PDF/UA-1 (ISO 14289-1) 标准。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String pdfComplianceName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int pdfCompliance)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int pdfCompliance)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### PDF_17 {#PDF-17}
```
public static int PDF_17
```


输出文件将符合 PDF 1.7 (ISO 32000-1) 标准。

### PDF_20 {#PDF-20}
```
public static int PDF_20
```


输出文件将符合 PDF 2.0 (ISO 32000-2) 标准。

### PDF_A_1_A {#PDF-A-1-A}
```
public static int PDF_A_1_A
```


输出文件将符合 PDF/A-1a (ISO 19005-1) 标准。此级别包括 PDF/A-1b 的所有要求，另外还要求包括文档结构（也称为“标记”），目的是确保文档内容可以被搜索和重新利用。请注意，导出文档结构会显着增加内存消耗，尤其是对于大型文档。

### PDF_A_1_B {#PDF-A-1-B}
```
public static int PDF_A_1_B
```


输出文件将符合 PDF/A-1b (ISO 19005-1) 标准。 PDF/A-1b 的目标是确保可靠地再现文档的视觉外观。

### PDF_A_2_A {#PDF-A-2-A}
```
public static int PDF_A_2_A
```


输出文件将符合 PDF/A-2a (ISO 19005-2) 标准。此级别包括 PDF/A-2u 的所有要求，另外还要求包括文档结构（也称为“标记”），目的是确保文档内容可以被搜索和重新利用。请注意，导出文档结构会显着增加内存消耗，尤其是对于大型文档。

### PDF_A_2_U {#PDF-A-2-U}
```
public static int PDF_A_2_U
```


输出文件将符合 PDF/A-2u (ISO 19005-2) 标准。 PDF/A-2u 的目标是随着时间的推移保留文档静态视觉外观，独立于用于创建、存储或呈现文件的工具和系统。此外，文档中包含的任何文本都可以可靠地提取为一系列 Unicode 代码点。

### PDF_A_4 {#PDF-A-4}
```
public static int PDF_A_4
```


输出文件将符合 PDF/A-4 (ISO 19005-4:2020) 标准。 PDF/A-4 的目标是随着时间的推移保持文档静态视觉外观，独立于用于创建、存储或呈现文件的工具和系统。此外，文档中包含的任何文本都可以可靠地提取为一系列 Unicode 代码点。

### PDF_UA_1 {#PDF-UA-1}
```
public static int PDF_UA_1
```


输出文件将符合 PDF/UA-1 (ISO 14289-1) 标准。 PDF/UA 的主要目的是定义如何以允许文件可访问的方式表示 PDF 格式的电子文档。

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
### fromName(String pdfComplianceName) {#fromName-java.lang.String-}
```
public static int fromName(String pdfComplianceName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pdfComplianceName | java.lang.String |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int pdfCompliance) {#getName-int-}
```
public static String getName(int pdfCompliance)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pdfCompliance | int |  |

**退货：**
java.lang.字符串
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
### toString(int pdfCompliance) {#toString-int-}
```
public static String toString(int pdfCompliance)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pdfCompliance | int |  |

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
