---
title: LoadFormat
second_title: Aspose.Words for Java API 参考
description: 指示要加载的文档的格式。
type: docs
weight: 377
url: /zh/java/com.aspose.words/loadformat/
---

**遗产：**
java.lang.Object
```
public class LoadFormat
```

指示要加载的文档的格式。
## 字段

| 场地 | 描述 |
| --- | --- |
| [AUTO](#AUTO) | 指示 Aspose.Words 自动识别格式。 |
| [AZW_3](#AZW-3) | AZW3 格式。 |
| [CHM](#CHM) | CHM（编译的 HTML 帮助）格式。 |
| [DOC](#DOC) | Microsoft Word 95 或 Word 97 - 2003 文档。 |
| [DOCM](#DOCM) | Office Open XML WordprocessingML 启用宏的文档。 |
| [DOCX](#DOCX) | Office Open XML WordprocessingML 文档（无宏）。 |
| [DOC_PRE_WORD_60](#DOC-PRE-WORD-60) | 该文档采用 Word 95 之前的格式。 |
| [DOT](#DOT) | Microsoft Word 95 或 Word 97 - 2003 模板。 |
| [DOTM](#DOTM) | Office Open XML WordprocessingML 启用宏的模板。 |
| [DOTX](#DOTX) | Office Open XML WordprocessingML 模板（无宏）。 |
| [EPUB](#EPUB) | EPUB 格式。 |
| [FLAT_OPC](#FLAT-OPC) | Office Open XML WordprocessingML 存储在平面 XML 文件而不是 ZIP 包中。 |
| [FLAT_OPC_MACRO_ENABLED](#FLAT-OPC-MACRO-ENABLED) | Office Open XML WordprocessingML 启用宏的文档存储在平面 XML 文件中，而不是 ZIP 包中。 |
| [FLAT_OPC_TEMPLATE](#FLAT-OPC-TEMPLATE) | Office Open XML WordprocessingML 模板（无宏）存储在平面 XML 文件而不是 ZIP 包中。 |
| [FLAT_OPC_TEMPLATE_MACRO_ENABLED](#FLAT-OPC-TEMPLATE-MACRO-ENABLED) | Office Open XML WordprocessingML 启用宏的模板存储在平面 XML 文件中，而不是 ZIP 包中。 |
| [HTML](#HTML) | HTML 格式。 |
| [MARKDOWN](#MARKDOWN) | 降价文本文档。 |
| [MHTML](#MHTML) | MHTML（Web 存档）格式。 |
| [MOBI](#MOBI) | 移动格式。 |
| [ODT](#ODT) | ODF 文本文档。 |
| [OTT](#OTT) | ODF 文本文档模板。 |
| [PDF](#PDF) | pdf文档。 |
| [RTF](#RTF) | RTF 格式。 |
| [TEXT](#TEXT) | 纯文本。 |
| [UNKNOWN](#UNKNOWN) | 无法识别的格式，无法由 Aspose.Words 加载。 |
| [WORD_ML](#WORD-ML) | Microsoft Word 2003 WordprocessingML 格式。 |
| [XML](#XML) | XML 文档。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String loadFormatName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int loadFormat)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int loadFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


指示 Aspose.Words 自动识别格式。

### AZW_3 {#AZW-3}
```
public static int AZW_3
```


AZW3 格式。由 Amazon Kindle 阅读器使用。

### CHM {#CHM}
```
public static int CHM
```


CHM（编译的 HTML 帮助）格式。

### DOC {#DOC}
```
public static int DOC
```


Microsoft Word 95 或 Word 97 - 2003 文档。

### DOCM {#DOCM}
```
public static int DOCM
```


Office Open XML WordprocessingML 启用宏的文档。

### DOCX {#DOCX}
```
public static int DOCX
```


Office Open XML WordprocessingML 文档（无宏）。

### DOC_PRE_WORD_60 {#DOC-PRE-WORD-60}
```
public static int DOC_PRE_WORD_60
```


该文档采用 Word 95 之前的格式。 Aspose.Words 目前不支持加载此类文档。

### DOT {#DOT}
```
public static int DOT
```


Microsoft Word 95 或 Word 97 - 2003 模板。

### DOTM {#DOTM}
```
public static int DOTM
```


Office Open XML WordprocessingML 启用宏的模板。

### DOTX {#DOTX}
```
public static int DOTX
```


Office Open XML WordprocessingML 模板（无宏）。

### EPUB {#EPUB}
```
public static int EPUB
```


EPUB 格式。

### FLAT_OPC {#FLAT-OPC}
```
public static int FLAT_OPC
```


Office Open XML WordprocessingML 存储在平面 XML 文件而不是 ZIP 包中。

### FLAT_OPC_MACRO_ENABLED {#FLAT-OPC-MACRO-ENABLED}
```
public static int FLAT_OPC_MACRO_ENABLED
```


Office Open XML WordprocessingML 启用宏的文档存储在平面 XML 文件中，而不是 ZIP 包中。

### FLAT_OPC_TEMPLATE {#FLAT-OPC-TEMPLATE}
```
public static int FLAT_OPC_TEMPLATE
```


Office Open XML WordprocessingML 模板（无宏）存储在平面 XML 文件而不是 ZIP 包中。

### FLAT_OPC_TEMPLATE_MACRO_ENABLED {#FLAT-OPC-TEMPLATE-MACRO-ENABLED}
```
public static int FLAT_OPC_TEMPLATE_MACRO_ENABLED
```


Office Open XML WordprocessingML 启用宏的模板存储在平面 XML 文件中，而不是 ZIP 包中。

### HTML {#HTML}
```
public static int HTML
```


HTML 格式。

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


降价文本文档。

### MHTML {#MHTML}
```
public static int MHTML
```


MHTML（Web 存档）格式。

### MOBI {#MOBI}
```
public static int MOBI
```


移动格式。由 MobiPocket 阅读器和 Amazon Kindle 阅读器使用。

### ODT {#ODT}
```
public static int ODT
```


ODF 文本文档。

### OTT {#OTT}
```
public static int OTT
```


ODF 文本文档模板。

### PDF {#PDF}
```
public static int PDF
```


pdf文档。

### RTF {#RTF}
```
public static int RTF
```


RTF 格式。

### TEXT {#TEXT}
```
public static int TEXT
```


纯文本。

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


无法识别的格式，无法由 Aspose.Words 加载。

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


Microsoft Word 2003 WordprocessingML 格式。

### XML {#XML}
```
public static int XML
```


XML 文档。

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
### fromName(String loadFormatName) {#fromName-java.lang.String-}
```
public static int fromName(String loadFormatName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| loadFormatName | java.lang.String |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int loadFormat) {#getName-int-}
```
public static String getName(int loadFormat)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| loadFormat | int |  |

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
### toString(int loadFormat) {#toString-int-}
```
public static String toString(int loadFormat)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| loadFormat | int |  |

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
