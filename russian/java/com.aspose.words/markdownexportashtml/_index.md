---
title: "MarkdownExportAsHtml"
linktitle: "MarkdownExportAsHtml"
second_title: "Aspose.Words для Java"
description: "Позволяет указать элементы, которые будут экспортированы в Markdown как необработанный HTML в Java."
type: docs
weight: 451
url: /ru/java/com.aspose.words/markdownexportashtml/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownExportAsHtml
```

Позволяет указать элементы, которые будут экспортированы в Markdown как необработанный HTML.

 **Examples:** 

Показывает, как экспортировать таблицу в Markdown как необработанный HTML.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Sample table:");

 // Create table.
 builder.insertCell();
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.RIGHT);
 builder.write("Cell1");
 builder.insertCell();
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write("Cell2");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setExportAsHtml(MarkdownExportAsHtml.TABLES);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportTableAsHtml.md", saveOptions);
 
```

Показывает, как экспортировать таблицы, которые нельзя корректно представить в чистом Markdown, как необработанный HTML.

```

 String outputPath = getArtifactsDir() + "MarkdownSaveOptions.NonCompatibleTables.md";

 Document doc = new Document(getMyDir() + "Non compatible table.docx");

 // With the "NonCompatibleTables" option, you can export tables that have a complex structure with merged cells
 // or nested tables to raw HTML and leave simple tables in Markdown format.
 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setExportAsHtml(MarkdownExportAsHtml.NON_COMPATIBLE_TABLES);

 doc.save(outputPath, saveOptions);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [NONE](#NONE) | Экспортировать все элементы, используя синтаксис Markdown, без какого-либо необработанного HTML. |
| [NON_COMPATIBLE_TABLES](#NON-COMPATIBLE-TABLES) | Экспортировать таблицы, которые нельзя корректно представить в чистом Markdown, как необработанный HTML. |
| [TABLES](#TABLES) | Экспортировать таблицы как необработанный HTML. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String markdownExportAsHtmlName)](#fromName-java.lang.String) |  |
| [fromNames(Set markdownExportAsHtmlNames)](#fromNames-java.util.Set) |  |
| [getName(int markdownExportAsHtml)](#getName-int) |  |
| [getNames(int markdownExportAsHtml)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownExportAsHtml)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Экспортировать все элементы, используя синтаксис Markdown, без какого-либо необработанного HTML.

### NON_COMPATIBLE_TABLES {#NON-COMPATIBLE-TABLES}
```
public static int NON_COMPATIBLE_TABLES
```


Экспортировать таблицы, которые нельзя корректно представить в чистом Markdown, как необработанный HTML.

 **Remarks:** 

Когда эта опция включена, Aspose.Words будет экспортировать только таблицы с объединёнными ячейками или вложенными таблицами как необработанный HTML. Все остальные таблицы будут экспортированы в формате Markdown. Также обратите внимание, что эта опция не сохраняет всё форматирование таблицы, а сохраняет только соответствующие диапазоны ячеек.

Если установлен связанный флаг [TABLES](../../com.aspose.words/markdownexportashtml/#TABLES), то этот флаг будет игнорироваться.

### TABLES {#TABLES}
```
public static int TABLES
```


Экспортировать таблицы как необработанный HTML.

 **Remarks:** 

Когда эта опция включена, каждая таблица будет экспортирована как необработанный HTML. Aspose.Words попытается сохранить всё форматирование таблиц в этом случае.

Если установлен этот флаг, то связанный флаг [NON_COMPATIBLE_TABLES](../../com.aspose.words/markdownexportashtml/#NON-COMPATIBLE-TABLES) будет игнорироваться.

### length {#length}
```
public static int length
```


### fromName(String markdownExportAsHtmlName) {#fromName-java.lang.String}
```
public static int fromName(String markdownExportAsHtmlName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| markdownExportAsHtmlName | java.lang.String |  |

**Returns:**
int
### fromNames(Set markdownExportAsHtmlNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set markdownExportAsHtmlNames)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| markdownExportAsHtmlNames | java.util.Set |  |

**Returns:**
int
### getName(int markdownExportAsHtml) {#getName-int}
```
public static String getName(int markdownExportAsHtml)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| markdownExportAsHtml | int |  |

**Returns:**
java.lang.String
### getNames(int markdownExportAsHtml) {#getNames-int}
```
public static Set getNames(int markdownExportAsHtml)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| markdownExportAsHtml | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int markdownExportAsHtml) {#toString-int}
```
public static String toString(int markdownExportAsHtml)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| markdownExportAsHtml | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
