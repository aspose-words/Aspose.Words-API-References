---
title: DocumentSplitCriteria
linktitle: DocumentSplitCriteria
second_title: Aspose.Words for Java
description: Specifies how the document is split into parts when saving to SaveFormat.HTML SaveFormat.EPUB or SaveFormat.AZW_3 format in Java.
type: docs
weight: 164
url: /java/com.aspose.words/documentsplitcriteria/
---

**Inheritance:**
java.lang.Object
```
public class DocumentSplitCriteria
```

Specifies how the document is split into parts when saving to [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB) or [SaveFormat.AZW\_3](../../com.aspose.words/saveformat/\#AZW-3) format.

 **Remarks:** 

[DocumentSplitCriteria](../../com.aspose.words/documentsplitcriteria/) is a set of flags which can be combined. For instance you can split the document at page breaks and heading paragraphs in the same export operation.

Different criteria can partially overlap. For instance, **Heading 1** style is frequently given [ParagraphFormat.getPageBreakBefore()](../../com.aspose.words/paragraphformat/\#getPageBreakBefore) / [ParagraphFormat.setPageBreakBefore(boolean)](../../com.aspose.words/paragraphformat/\#setPageBreakBefore-boolean) property so it falls under two criteria: [PAGE\_BREAK](../../com.aspose.words/documentsplitcriteria/\#PAGE-BREAK) and [HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria/\#HEADING-PARAGRAPH). Some section breaks can cause page breaks and so on. In typical cases specifying only one flag is the most practical option.

 **Examples:** 

Shows how to use a specific encoding when saving a document to .epub.

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
## Fields

| Field | Description |
| --- | --- |
| [COLUMN_BREAK](#COLUMN-BREAK) | The document is split into parts at column breaks. |
| [HEADING_PARAGRAPH](#HEADING-PARAGRAPH) | The document is split into parts at a paragraph formatted using a heading style **Heading 1**, **Heading 2** etc. |
| [NONE](#NONE) | The document is not split. |
| [PAGE_BREAK](#PAGE-BREAK) | The document is split into parts at explicit page breaks. |
| [SECTION_BREAK](#SECTION-BREAK) | The document is split into parts at a section break of any type. |
| [length](#length) |  |
## Methods

| Method | Description |
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


The document is split into parts at column breaks. A column break can be specified by a [ControlChar.COLUMN\_BREAK](../../com.aspose.words/controlchar/\#COLUMN-BREAK) character or a section break specifying start of new section in a new column.

### HEADING_PARAGRAPH {#HEADING-PARAGRAPH}
```
public static int HEADING_PARAGRAPH
```


The document is split into parts at a paragraph formatted using a heading style **Heading 1**, **Heading 2** etc. Use together with [HtmlSaveOptions.getDocumentSplitHeadingLevel()](../../com.aspose.words/htmlsaveoptions/\#getDocumentSplitHeadingLevel) / [HtmlSaveOptions.setDocumentSplitHeadingLevel(int)](../../com.aspose.words/htmlsaveoptions/\#setDocumentSplitHeadingLevel-int) to specify the heading levels (from 1 to the specified level) at which to split.

### NONE {#NONE}
```
public static int NONE
```


The document is not split.

### PAGE_BREAK {#PAGE-BREAK}
```
public static int PAGE_BREAK
```


The document is split into parts at explicit page breaks. A page break can be specified by a [ControlChar.PAGE\_BREAK](../../com.aspose.words/controlchar/\#PAGE-BREAK) character, a section break specifying start of new section on a new page, or a paragraph that has its [ParagraphFormat.getPageBreakBefore()](../../com.aspose.words/paragraphformat/\#getPageBreakBefore) / [ParagraphFormat.setPageBreakBefore(boolean)](../../com.aspose.words/paragraphformat/\#setPageBreakBefore-boolean) property set to  true .

### SECTION_BREAK {#SECTION-BREAK}
```
public static int SECTION_BREAK
```


The document is split into parts at a section break of any type.

### length {#length}
```
public static int length
```


### fromName(String documentSplitCriteriaName) {#fromName-java.lang.String}
```
public static int fromName(String documentSplitCriteriaName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentSplitCriteriaName | java.lang.String |  |

**Returns:**
int
### fromNames(Set documentSplitCriteriaNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set documentSplitCriteriaNames)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentSplitCriteriaNames | java.util.Set |  |

**Returns:**
int
### getName(int documentSplitCriteria) {#getName-int}
```
public static String getName(int documentSplitCriteria)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentSplitCriteria | int |  |

**Returns:**
java.lang.String
### getNames(int documentSplitCriteria) {#getNames-int}
```
public static Set getNames(int documentSplitCriteria)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| documentSplitCriteria | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
