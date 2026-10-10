---
title: "DocumentSplitCriteria"
linktitle: "DocumentSplitCriteria"
second_title: "Aspose.Words per Java"
description: "Specifica come il documento viene suddiviso in parti durante il salvataggio nel formato SaveFormat.HTML, SaveFormat.EPUB o SaveFormat.AZW_3 in Java."
type: docs
weight: 174
url: /it/java/com.aspose.words/documentsplitcriteria/
---

**Inheritance:**
java.lang.Object
```
public class DocumentSplitCriteria
```

Specifica come il documento viene suddiviso in parti durante il salvataggio nel formato [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB), o [SaveFormat.AZW\_3](../../com.aspose.words/saveformat/\#AZW-3).

 **Remarks:** 

[DocumentSplitCriteria](../../com.aspose.words/documentsplitcriteria/) is a set of flags which can be combined. For instance you can split the document at page breaks and heading paragraphs in the same export operation.

Diversi criteri possono sovrapporsi parzialmente. Per esempio, lo stile **Heading 1** viene spesso associato alla proprietà [ParagraphFormat.getPageBreakBefore()](../../com.aspose.words/paragraphformat/\#getPageBreakBefore) / [ParagraphFormat.setPageBreakBefore(boolean)](../../com.aspose.words/paragraphformat/\#setPageBreakBefore-boolean) in modo che rientri in due criteri: [PAGE\_BREAK](../../com.aspose.words/documentsplitcriteria/\#PAGE-BREAK) e [HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria/\#HEADING-PARAGRAPH). Alcuni interruzioni di sezione possono causare interruzioni di pagina e così via. Nei casi tipici, specificare un solo flag è l'opzione più pratica.

 **Examples:** 

Mostra come utilizzare una codifica specifica durante il salvataggio di un documento in .epub.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [COLUMN_BREAK](#COLUMN-BREAK) | Il documento è suddiviso in parti alle interruzioni di colonna. |
| [HEADING_PARAGRAPH](#HEADING-PARAGRAPH) | Il documento è suddiviso in parti a un paragrafo formattato con uno stile di intestazione **Heading 1**, **Heading 2** ecc. |
| [NONE](#NONE) | Il documento non è suddiviso. |
| [PAGE_BREAK](#PAGE-BREAK) | Il documento è suddiviso in parti alle interruzioni di pagina esplicite. |
| [SECTION_BREAK](#SECTION-BREAK) | Il documento è suddiviso in parti a un'interruzione di sezione di qualsiasi tipo. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
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


Il documento è suddiviso in parti alle interruzioni di colonna. Un'interruzione di colonna può essere specificata da un carattere [ControlChar.COLUMN\_BREAK](../../com.aspose.words/controlchar/\#COLUMN-BREAK) o da un'interruzione di sezione che indica l'inizio di una nuova sezione in una nuova colonna.

### HEADING_PARAGRAPH {#HEADING-PARAGRAPH}
```
public static int HEADING_PARAGRAPH
```


Il documento è suddiviso in parti a un paragrafo formattato con uno stile di intestazione **Heading 1**, **Heading 2** ecc. Utilizzare insieme a [HtmlSaveOptions.getDocumentSplitHeadingLevel()](../../com.aspose.words/htmlsaveoptions/\#getDocumentSplitHeadingLevel) / [HtmlSaveOptions.setDocumentSplitHeadingLevel(int)](../../com.aspose.words/htmlsaveoptions/\#setDocumentSplitHeadingLevel-int) per specificare i livelli di intestazione (da 1 al livello specificato) in cui effettuare la suddivisione.

### NONE {#NONE}
```
public static int NONE
```


Il documento non è suddiviso.

### PAGE_BREAK {#PAGE-BREAK}
```
public static int PAGE_BREAK
```


Il documento è suddiviso in parti alle interruzioni di pagina esplicite. Un'interruzione di pagina può essere specificata da un carattere [ControlChar.PAGE\_BREAK](../../com.aspose.words/controlchar/\#PAGE-BREAK), da un'interruzione di sezione che indica l'inizio di una nuova sezione su una nuova pagina, o da un paragrafo che ha la proprietà [ParagraphFormat.getPageBreakBefore()](../../com.aspose.words/paragraphformat/\#getPageBreakBefore) / [ParagraphFormat.setPageBreakBefore(boolean)](../../com.aspose.words/paragraphformat/\#setPageBreakBefore-boolean) impostata su true.

### SECTION_BREAK {#SECTION-BREAK}
```
public static int SECTION_BREAK
```


Il documento è suddiviso in parti a un'interruzione di sezione di qualsiasi tipo.

### length {#length}
```
public static int length
```


### fromName(String documentSplitCriteriaName) {#fromName-java.lang.String}
```
public static int fromName(String documentSplitCriteriaName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| documentSplitCriteriaName | java.lang.String |  |

**Returns:**
int
### fromNames(Set documentSplitCriteriaNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set documentSplitCriteriaNames)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| documentSplitCriteriaNames | java.util.Set |  |

**Returns:**
int
### getName(int documentSplitCriteria) {#getName-int}
```
public static String getName(int documentSplitCriteria)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| documentSplitCriteria | int |  |

**Returns:**
java.lang.String
### getNames(int documentSplitCriteria) {#getNames-int}
```
public static Set getNames(int documentSplitCriteria)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| documentSplitCriteria | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
