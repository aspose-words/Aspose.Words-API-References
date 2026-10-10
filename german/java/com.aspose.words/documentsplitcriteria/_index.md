---
title: "DocumentSplitCriteria"
linktitle: "DocumentSplitCriteria"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie das Dokument beim Speichern im Format SaveFormat.HTML, SaveFormat.EPUB oder SaveFormat.AZW_3 in Java in Teile aufgeteilt wird."
type: docs
weight: 174
url: /de/java/com.aspose.words/documentsplitcriteria/
---

**Inheritance:**
java.lang.Object
```
public class DocumentSplitCriteria
```

Gibt an, wie das Dokument beim Speichern im Format [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB) oder [SaveFormat.AZW\_3](../../com.aspose.words/saveformat/\#AZW-3) aufgeteilt wird.

 **Remarks:** 

[DocumentSplitCriteria](../../com.aspose.words/documentsplitcriteria/) is a set of flags which can be combined. For instance you can split the document at page breaks and heading paragraphs in the same export operation.

Verschiedene Kriterien können teilweise überlappen. Zum Beispiel wird dem Stil **Heading 1** häufig die Eigenschaft [ParagraphFormat.getPageBreakBefore()](../../com.aspose.words/paragraphformat/\#getPageBreakBefore) / [ParagraphFormat.setPageBreakBefore(boolean)](../../com.aspose.words/paragraphformat/\#setPageBreakBefore-boolean) zugewiesen, sodass er unter zwei Kriterien fällt: [PAGE\_BREAK](../../com.aspose.words/documentsplitcriteria/\#PAGE-BREAK) und [HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria/\#HEADING-PARAGRAPH). Einige Abschnittsumbrüche können Seitenumbrüche verursachen usw. In typischen Fällen ist das Angeben nur eines Flags die praktischste Option.

 **Examples:** 

Zeigt, wie man beim Speichern eines Dokuments als .epub eine bestimmte Kodierung verwendet.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [COLUMN_BREAK](#COLUMN-BREAK) | Das Dokument wird an Spaltenumbrüchen in Teile aufgeteilt. |
| [HEADING_PARAGRAPH](#HEADING-PARAGRAPH) | Das Dokument wird an einem Absatz, der mit einer Überschriftenformatierung **Heading 1**, **Heading 2** usw. formatiert ist, in Teile aufgeteilt. |
| [NONE](#NONE) | Das Dokument wird nicht aufgeteilt. |
| [PAGE_BREAK](#PAGE-BREAK) | Das Dokument wird an expliziten Seitenumbrüchen in Teile aufgeteilt. |
| [SECTION_BREAK](#SECTION-BREAK) | Das Dokument wird an einem Abschnittsumbruch beliebigen Typs in Teile aufgeteilt. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
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


Das Dokument wird an Spaltenumbrüchen in Teile aufgeteilt. Ein Spaltenumbruch kann durch ein [ControlChar.COLUMN\_BREAK](../../com.aspose.words/controlchar/\#COLUMN-BREAK) Zeichen oder einen Abschnittsumbruch, der den Beginn eines neuen Abschnitts in einer neuen Spalte angibt, spezifiziert werden.

### HEADING_PARAGRAPH {#HEADING-PARAGRAPH}
```
public static int HEADING_PARAGRAPH
```


Das Dokument wird an einem Absatz, der mit einer Überschriftenformatierung **Heading 1**, **Heading 2** usw. formatiert ist, in Teile aufgeteilt. Verwenden Sie es zusammen mit [HtmlSaveOptions.getDocumentSplitHeadingLevel()](../../com.aspose.words/htmlsaveoptions/\#getDocumentSplitHeadingLevel) / [HtmlSaveOptions.setDocumentSplitHeadingLevel(int)](../../com.aspose.words/htmlsaveoptions/\#setDocumentSplitHeadingLevel-int), um die Überschriftenebenen (von 1 bis zur angegebenen Ebene) anzugeben, bei denen aufgeteilt werden soll.

### NONE {#NONE}
```
public static int NONE
```


Das Dokument wird nicht aufgeteilt.

### PAGE_BREAK {#PAGE-BREAK}
```
public static int PAGE_BREAK
```


Das Dokument wird bei expliziten Seitenumbrüchen in Teile aufgeteilt. Ein Seitenumbruch kann durch ein [ControlChar.PAGE\_BREAK](../../com.aspose.words/controlchar/\#PAGE-BREAK) Zeichen, einen Abschnittswechsel, der den Beginn eines neuen Abschnitts auf einer neuen Seite angibt, oder einen Absatz, dessen [ParagraphFormat.getPageBreakBefore()](../../com.aspose.words/paragraphformat/\#getPageBreakBefore) / [ParagraphFormat.setPageBreakBefore(boolean)](../../com.aspose.words/paragraphformat/\#setPageBreakBefore-boolean) Eigenschaft auf true gesetzt ist, spezifiziert werden.

### SECTION_BREAK {#SECTION-BREAK}
```
public static int SECTION_BREAK
```


Das Dokument wird an einem Abschnittsumbruch beliebigen Typs in Teile aufgeteilt.

### length {#length}
```
public static int length
```


### fromName(String documentSplitCriteriaName) {#fromName-java.lang.String}
```
public static int fromName(String documentSplitCriteriaName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| documentSplitCriteriaName | java.lang.String |  |

**Returns:**
int
### fromNames(Set documentSplitCriteriaNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set documentSplitCriteriaNames)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| documentSplitCriteriaNames | java.util.Set |  |

**Returns:**
int
### getName(int documentSplitCriteria) {#getName-int}
```
public static String getName(int documentSplitCriteria)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| documentSplitCriteria | int |  |

**Returns:**
java.lang.String
### getNames(int documentSplitCriteria) {#getNames-int}
```
public static Set getNames(int documentSplitCriteria)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| documentSplitCriteria | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
