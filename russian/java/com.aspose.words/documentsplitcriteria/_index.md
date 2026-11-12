---
title: "DocumentSplitCriteria"
linktitle: "DocumentSplitCriteria"
second_title: "Aspose.Words для Java"
description: "Указывает, как документ разбивается на части при сохранении в формат SaveFormat.HTML, SaveFormat.EPUB или SaveFormat.AZW_3 в Java."
type: docs
weight: 174
url: /ru/java/com.aspose.words/documentsplitcriteria/
---

**Inheritance:**
java.lang.Object
```
public class DocumentSplitCriteria
```

Указывает, как документ разбивается на части при сохранении в формат [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB) или [SaveFormat.AZW\_3](../../com.aspose.words/saveformat/\#AZW-3) формат.

 **Remarks:** 

[DocumentSplitCriteria](../../com.aspose.words/documentsplitcriteria/) is a set of flags which can be combined. For instance you can split the document at page breaks and heading paragraphs in the same export operation.

Разные критерии могут частично перекрываться. Например, стиль **Heading 1** часто получает свойство [ParagraphFormat.getPageBreakBefore()](../../com.aspose.words/paragraphformat/\#getPageBreakBefore) / [ParagraphFormat.setPageBreakBefore(boolean)](../../com.aspose.words/paragraphformat/\#setPageBreakBefore-boolean) , поэтому он попадает под два критерия: [PAGE\_BREAK](../../com.aspose.words/documentsplitcriteria/\#PAGE-BREAK) и [HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria/\#HEADING-PARAGRAPH). Некоторые разрывы разделов могут вызывать разрывы страниц и т.д. В типичных случаях указание только одного флага является наиболее практичным вариантом.

 **Examples:** 

Показывает, как использовать определённую кодировку при сохранении документа в .epub.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Use a SaveOptions object to specify the encoding for a document that we will save.
 HtmlSaveOptions saveOptions = new HtmlSaveOptions();
 saveOptions.setSaveFormat(SaveFormat.EPUB);
 saveOptions.setEncoding(StandardCharsets.UTF_8);

 // By default, an output .epub document will have all of its contents in one HTML part.
 // A split criterion allows us to segment the document into several HTML parts.
 // We will set the criteria to split the document into heading paragraphs.
 // This is useful for readers who cannot read HTML files more significant than a specific size.
 saveOptions.setDocumentSplitCriteria(DocumentSplitCriteria.HEADING_PARAGRAPH);

 // Specify that we want to export document properties.
 saveOptions.setExportDocumentProperties(true);

 doc.save(getArtifactsDir() + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [COLUMN_BREAK](#COLUMN-BREAK) | Документ разбивается на части при разрывах колонок. |
| [HEADING_PARAGRAPH](#HEADING-PARAGRAPH) | Документ разбивается на части в абзаце, отформатированном с помощью стиля заголовка **Heading 1**, **Heading 2** и т.д. |
| [NONE](#NONE) | Документ не разбивается. |
| [PAGE_BREAK](#PAGE-BREAK) | Документ разбивается на части при явных разрывах страниц. |
| [SECTION_BREAK](#SECTION-BREAK) | Документ разбивается на части при разрыве раздела любого типа. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String documentSplitCriteriaName)](#fromName-java.lang.String) |  |
| [fromNames(Set documentSplitCriteriaNames)](#fromNames-java.util.Set) |  |
| [getName(int documentSplitCriteria)](#getName-int) |  |
| [getNames(int documentSplitCriteria)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int documentSplitCriteria)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### COLUMN_BREAK {#COLUMN-BREAK}
```
public static int COLUMN_BREAK
```


Документ разбивается на части при разрывах колонок. Разрыв колонки можно задать символом [ControlChar.COLUMN\_BREAK](../../com.aspose.words/controlchar/\#COLUMN-BREAK) или разрывом раздела, указывающим начало нового раздела в новой колонке.

### HEADING_PARAGRAPH {#HEADING-PARAGRAPH}
```
public static int HEADING_PARAGRAPH
```


Документ разбивается на части в абзаце, отформатированном стилем заголовка **Heading 1**, **Heading 2** и т.д. Используйте совместно с [HtmlSaveOptions.getDocumentSplitHeadingLevel()](../../com.aspose.words/htmlsaveoptions/\#getDocumentSplitHeadingLevel) / [HtmlSaveOptions.setDocumentSplitHeadingLevel(int)](../../com.aspose.words/htmlsaveoptions/\#setDocumentSplitHeadingLevel-int) для указания уровней заголовков (от 1 до указанного уровня), на которых выполнять разбиение.

### NONE {#NONE}
```
public static int NONE
```


Документ не разбивается.

### PAGE_BREAK {#PAGE-BREAK}
```
public static int PAGE_BREAK
```


Документ разбивается на части при явных разрывах страниц. Разрыв страницы можно задать символом [ControlChar.PAGE\_BREAK](../../com.aspose.words/controlchar/\#PAGE-BREAK) , разрывом раздела, указывающим начало нового раздела на новой странице, или абзацем, у которого свойство [ParagraphFormat.getPageBreakBefore()](../../com.aspose.words/paragraphformat/\#getPageBreakBefore) / [ParagraphFormat.setPageBreakBefore(boolean)](../../com.aspose.words/paragraphformat/\#setPageBreakBefore-boolean) установлено в true .

### SECTION_BREAK {#SECTION-BREAK}
```
public static int SECTION_BREAK
```


Документ разбивается на части при разрыве раздела любого типа.

### length {#length}
```
public static int length
```


### fromName(String documentSplitCriteriaName) {#fromName-java.lang.String}
```
public static int fromName(String documentSplitCriteriaName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| documentSplitCriteriaName | java.lang.String |  |

**Returns:**
int
### fromNames(Set documentSplitCriteriaNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set documentSplitCriteriaNames)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| documentSplitCriteriaNames | java.util.Set |  |

**Returns:**
int
### getName(int documentSplitCriteria) {#getName-int}
```
public static String getName(int documentSplitCriteria)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| documentSplitCriteria | int |  |

**Returns:**
java.lang.String
### getNames(int documentSplitCriteria) {#getNames-int}
```
public static Set getNames(int documentSplitCriteria)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| documentSplitCriteria | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int documentSplitCriteria) {#toString-int}
```
public static String toString(int documentSplitCriteria)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| documentSplitCriteria | int |  |

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
