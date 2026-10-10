---
title: "HeaderFooterBookmarksExportMode"
linktitle: "HeaderFooterBookmarksExportMode"
second_title: "Aspose.Words для Java"
description: "Указывает, как закладки в верхних/нижних колонтитулах экспортируются в Java."
type: docs
weight: 370
url: /ru/java/com.aspose.words/headerfooterbookmarksexportmode/
---

**Inheritance:**
java.lang.Object
```
public class HeaderFooterBookmarksExportMode
```

Указывает, как экспортируются закладки в верхних/нижних колонтитулах.

 **Examples:** 

Показывает, как обрабатывать закладки в верхних/нижних колонтитулах в документе, который мы рендерим в PDF.

```

 Document doc = new Document(getMyDir() + "Bookmarks in headers and footers.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Set the "PageMode" property to "PdfPageMode.UseOutlines" to display the outline navigation pane in the output PDF.
 saveOptions.setPageMode(PdfPageMode.USE_OUTLINES);

 // Set the "DefaultBookmarksOutlineLevel" property to "1" to display all
 // bookmarks at the first level of the outline in the output PDF.
 saveOptions.getOutlineOptions().setDefaultBookmarksOutlineLevel(1);

 // Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.None" to
 // not export any bookmarks that are inside headers/footers.
 // Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.First" to
 // only export bookmarks in the first section's header/footers.
 // Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.All" to
 // export bookmarks that are in all headers/footers.
 saveOptions.setHeaderFooterBookmarksExportMode(headerFooterBookmarksExportMode);

 doc.save(getArtifactsDir() + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [ALL](#ALL) | Закладки во всех верхних/нижних колонтитулах экспортируются. |
| [FIRST](#FIRST) | Экспортируется только закладка в первом верхнем/нижнем колонтитуле раздела. |
| [NONE](#NONE) | Закладки в верхних/нижних колонтитулах не экспортируются. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String headerFooterBookmarksExportModeName)](#fromName-java.lang.String) |  |
| [getName(int headerFooterBookmarksExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int headerFooterBookmarksExportMode)](#toString-int) |  |
### ALL {#ALL}
```
public static int ALL
```


Закладки во всех верхних/нижних колонтитулах экспортируются.

### FIRST {#FIRST}
```
public static int FIRST
```


Экспортируется только закладка в первом верхнем/нижнем колонтитуле раздела.

### NONE {#NONE}
```
public static int NONE
```


Закладки в верхних/нижних колонтитулах не экспортируются.

### length {#length}
```
public static int length
```


### fromName(String headerFooterBookmarksExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String headerFooterBookmarksExportModeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| headerFooterBookmarksExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int headerFooterBookmarksExportMode) {#getName-int}
```
public static String getName(int headerFooterBookmarksExportMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| headerFooterBookmarksExportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int headerFooterBookmarksExportMode) {#toString-int}
```
public static String toString(int headerFooterBookmarksExportMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| headerFooterBookmarksExportMode | int |  |

**Returns:**
java.lang.String
