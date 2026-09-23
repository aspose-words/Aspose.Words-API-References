---
title: "DocumentSplitCriteria"
linktitle: "DocumentSplitCriteria"
second_title: "Aspose.Words pour Java"
description: "Spécifie comment le document est divisé en parties lors de l'enregistrement au format SaveFormat.HTML SaveFormat.EPUB ou SaveFormat.AZW_3 en Java."
type: docs
weight: 174
url: /fr/java/com.aspose.words/documentsplitcriteria/
---

**Inheritance:**
java.lang.Object
```
public class DocumentSplitCriteria
```

Spécifie comment le document est divisé en parties lors de l'enregistrement au format [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB) ou [SaveFormat.AZW\_3](../../com.aspose.words/saveformat/\#AZW-3).

 **Remarks:** 

[DocumentSplitCriteria](../../com.aspose.words/documentsplitcriteria/) is a set of flags which can be combined. For instance you can split the document at page breaks and heading paragraphs in the same export operation.

Différents critères peuvent se chevaucher partiellement. Par exemple, le style **Heading 1** reçoit fréquemment la propriété [ParagraphFormat.getPageBreakBefore()](../../com.aspose.words/paragraphformat/\#getPageBreakBefore) / [ParagraphFormat.setPageBreakBefore(boolean)](../../com.aspose.words/paragraphformat/\#setPageBreakBefore-boolean) de sorte qu'il relève de deux critères : [PAGE\_BREAK](../../com.aspose.words/documentsplitcriteria/\#PAGE-BREAK) et [HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria/\#HEADING-PARAGRAPH). Certains sauts de section peuvent provoquer des sauts de page, etc. Dans la plupart des cas, spécifier un seul indicateur est l'option la plus pratique.

 **Examples:** 

Montre comment utiliser un encodage spécifique lors de l'enregistrement d'un document au format .epub.

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
## Champs

| Champ | Description |
| --- | --- |
| [COLUMN_BREAK](#COLUMN-BREAK) | Le document est divisé en parties aux sauts de colonne. |
| [HEADING_PARAGRAPH](#HEADING-PARAGRAPH) | Le document est divisé en parties à un paragraphe formaté avec un style de titre **Heading 1**, **Heading 2**, etc. |
| [NONE](#NONE) | Le document n'est pas divisé. |
| [PAGE_BREAK](#PAGE-BREAK) | Le document est divisé en parties aux sauts de page explicites. |
| [SECTION_BREAK](#SECTION-BREAK) | Le document est divisé en parties à un saut de section de tout type. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
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


Le document est divisé en parties aux sauts de colonne. Un saut de colonne peut être spécifié par le caractère [ControlChar.COLUMN\_BREAK](../../com.aspose.words/controlchar/\#COLUMN-BREAK) ou par un saut de section indiquant le début d'une nouvelle section dans une nouvelle colonne.

### HEADING_PARAGRAPH {#HEADING-PARAGRAPH}
```
public static int HEADING_PARAGRAPH
```


Le document est divisé en parties à un paragraphe formaté avec un style de titre **Heading 1**, **Heading 2**, etc. Utilisez-le conjointement avec [HtmlSaveOptions.getDocumentSplitHeadingLevel()](../../com.aspose.words/htmlsaveoptions/\#getDocumentSplitHeadingLevel) / [HtmlSaveOptions.setDocumentSplitHeadingLevel(int)](../../com.aspose.words/htmlsaveoptions/\#setDocumentSplitHeadingLevel-int) pour spécifier les niveaux de titre (de 1 au niveau indiqué) où effectuer la division.

### NONE {#NONE}
```
public static int NONE
```


Le document n'est pas divisé.

### PAGE_BREAK {#PAGE-BREAK}
```
public static int PAGE_BREAK
```


Le document est divisé en parties aux sauts de page explicites. Un saut de page peut être spécifié par le caractère [ControlChar.PAGE\_BREAK](../../com.aspose.words/controlchar/\#PAGE-BREAK) un saut de section indiquant le début d'une nouvelle section sur une nouvelle page, ou un paragraphe dont la propriété [ParagraphFormat.getPageBreakBefore()](../../com.aspose.words/paragraphformat/\#getPageBreakBefore) / [ParagraphFormat.setPageBreakBefore(boolean)](../../com.aspose.words/paragraphformat/\#setPageBreakBefore-boolean) est définie sur true.

### SECTION_BREAK {#SECTION-BREAK}
```
public static int SECTION_BREAK
```


Le document est divisé en parties à un saut de section de tout type.

### length {#length}
```
public static int length
```


### fromName(String documentSplitCriteriaName) {#fromName-java.lang.String}
```
public static int fromName(String documentSplitCriteriaName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| documentSplitCriteriaName | java.lang.String |  |

**Returns:**
int
### fromNames(Set documentSplitCriteriaNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set documentSplitCriteriaNames)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| documentSplitCriteriaNames | java.util.Set |  |

**Returns:**
int
### getName(int documentSplitCriteria) {#getName-int}
```
public static String getName(int documentSplitCriteria)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| documentSplitCriteria | int |  |

**Returns:**
java.lang.String
### getNames(int documentSplitCriteria) {#getNames-int}
```
public static Set getNames(int documentSplitCriteria)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| documentSplitCriteria | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
