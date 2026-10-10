---
title: "MarkdownLinkExportMode"
linktitle: "MarkdownLinkExportMode"
second_title: "Aspose.Words для Java"
description: "Указывает, как ссылки экспортируются в Markdown в Java."
type: docs
weight: 452
url: /ru/java/com.aspose.words/markdownlinkexportmode/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownLinkExportMode
```

Указывает, как ссылки экспортируются в Markdown.

 **Examples:** 

Показывает, как ссылки будут записываться в файл .md.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertShape(ShapeType.BALLOON, 100.0, 100.0);

 // Image will be written as reference:
 // ![ref1]
 //
 // [ref1]: aw_ref.001.png
 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setLinkExportMode(MarkdownLinkExportMode.REFERENCE);
 doc.save(getArtifactsDir() + "MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

 // Image will be written as inline:
 // ![](../aw_inline.001.png)
 saveOptions.setLinkExportMode(MarkdownLinkExportMode.INLINE);
 doc.save(getArtifactsDir() + "MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [AUTO](#AUTO) | Автоматически определять режим экспорта для каждой ссылки. |
| [INLINE](#INLINE) | Экспортировать все ссылки как встроенные блоки. |
| [REFERENCE](#REFERENCE) | Экспортировать все ссылки как ссылочные блоки. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String markdownLinkExportModeName)](#fromName-java.lang.String) |  |
| [getName(int markdownLinkExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownLinkExportMode)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Автоматически определять режим экспорта для каждой ссылки.

### INLINE {#INLINE}
```
public static int INLINE
```


Экспортировать все ссылки как встроенные блоки.

### REFERENCE {#REFERENCE}
```
public static int REFERENCE
```


Экспортировать все ссылки как ссылочные блоки.

### length {#length}
```
public static int length
```


### fromName(String markdownLinkExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String markdownLinkExportModeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| markdownLinkExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int markdownLinkExportMode) {#getName-int}
```
public static String getName(int markdownLinkExportMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| markdownLinkExportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int markdownLinkExportMode) {#toString-int}
```
public static String toString(int markdownLinkExportMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| markdownLinkExportMode | int |  |

**Returns:**
java.lang.String
