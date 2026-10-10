---
title: "XlsxDateTimeParsingMode"
linktitle: "XlsxDateTimeParsingMode"
second_title: "Aspose.Words for Java"
description: "指定在 Java 中如何解析文档文本以识别日期和时间值。"
type: docs
weight: 742
url: /zh/java/com.aspose.words/xlsxdatetimeparsingmode/
---

**Inheritance:**
java.lang.Object
```
public class XlsxDateTimeParsingMode
```

指定如何解析文档文本以识别日期和时间值。

 **Examples:** 

展示如何指定日期时间格式的自动检测。

```

 Document doc = new Document(getMyDir() + "Xlsx DateTime.docx");

 XlsxSaveOptions saveOptions = new XlsxSaveOptions();
 // Specify using datetime format autodetection.
 saveOptions.setDateTimeParsingMode(XlsxDateTimeParsingMode.AUTO);

 doc.save(getArtifactsDir() + "XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
 
```
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [AUTO](#AUTO) | 文档中使用的日期时间格式会自动确定。 |
| [USE_CURRENT_LOCALE](#USE-CURRENT-LOCALE) | 首先使用为当前线程设置的日期时间格式来解析字符串值。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String xlsxDateTimeParsingModeName)](#fromName-java.lang.String) |  |
| [getName(int xlsxDateTimeParsingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int xlsxDateTimeParsingMode)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


文档中使用的日期时间格式会自动确定。这可能会花费额外的时间。

### USE_CURRENT_LOCALE {#USE-CURRENT-LOCALE}
```
public static int USE_CURRENT_LOCALE
```


首先使用为当前线程设置的日期时间格式来解析字符串值。如果解析失败，将尝试其他常见的日期时间格式。

### length {#length}
```
public static int length
```


### fromName(String xlsxDateTimeParsingModeName) {#fromName-java.lang.String}
```
public static int fromName(String xlsxDateTimeParsingModeName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| xlsxDateTimeParsingModeName | java.lang.String |  |

**Returns:**
int
### getName(int xlsxDateTimeParsingMode) {#getName-int}
```
public static String getName(int xlsxDateTimeParsingMode)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| xlsxDateTimeParsingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int xlsxDateTimeParsingMode) {#toString-int}
```
public static String toString(int xlsxDateTimeParsingMode)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| xlsxDateTimeParsingMode | int |  |

**Returns:**
java.lang.String
