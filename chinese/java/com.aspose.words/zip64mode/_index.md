---
title: "Zip64Mode"
linktitle: "Zip64Mode"
second_title: "Aspose.Words for Java"
description: "指定何时在 Java 中对 OOXML 文件使用 ZIP64 格式扩展。"
type: docs
weight: 750
url: /zh/java/com.aspose.words/zip64mode/
---

**Inheritance:**
java.lang.Object
```
public class Zip64Mode
```

指定何时对 OOXML 文件使用 ZIP64 格式扩展。

 **Remarks:** 

OOXML 文件是一个 ZIP 存档，对单个文件的未压缩大小、压缩大小以及归档的总大小都有 4 GB（2^32 字节）的限制，并且归档中的文件数量限制为 65,535（2^16-1）个。ZIP64 格式扩展将这些限制提升至 2^64。

 **Examples:** 

展示如何使用 ZIP64 格式扩展。

```

 Random random = new Random();
 DocumentBuilder builder = new DocumentBuilder();

 for (int i = 0; i < 10000; i++)
 {
     BufferedImage bmp = new BufferedImage(5, 5, BufferedImage.TYPE_INT_ARGB);
     Graphics2D g = bmp.createGraphics();
     g.setColor(new Color(random.nextInt(254), random.nextInt(254), random.nextInt(254)));
     g.drawImage(bmp, 0, 0, null);
     g.dispose();
     builder.insertImage(bmp);
 }

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 saveOptions.setZip64Mode(Zip64Mode.ALWAYS);

 builder.getDocument().save(getArtifactsDir() + "OoxmlSaveOptions.Zip64ModeOption.docx", saveOptions);
 
```
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [ALWAYS](#ALWAYS) | 始终使用 ZIP64 格式扩展。 |
| [IF_NECESSARY](#IF-NECESSARY) | 如有必要，使用 ZIP64 格式扩展。 |
| [NEVER](#NEVER) | 不要使用 ZIP64 格式扩展。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String zip64ModeName)](#fromName-java.lang.String) |  |
| [getName(int zip64Mode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int zip64Mode)](#toString-int) |  |
### ALWAYS {#ALWAYS}
```
public static int ALWAYS
```


始终使用 ZIP64 格式扩展。

### IF_NECESSARY {#IF-NECESSARY}
```
public static int IF_NECESSARY
```


如有必要，使用 ZIP64 格式扩展。

### NEVER {#NEVER}
```
public static int NEVER
```


不要使用 ZIP64 格式扩展。

### length {#length}
```
public static int length
```


### fromName(String zip64ModeName) {#fromName-java.lang.String}
```
public static int fromName(String zip64ModeName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| zip64ModeName | java.lang.String |  |

**Returns:**
int
### getName(int zip64Mode) {#getName-int}
```
public static String getName(int zip64Mode)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| zip64Mode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int zip64Mode) {#toString-int}
```
public static String toString(int zip64Mode)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| zip64Mode | int |  |

**Returns:**
java.lang.String
