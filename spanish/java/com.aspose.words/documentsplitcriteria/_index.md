---
title: "DocumentSplitCriteria"
linktitle: "DocumentSplitCriteria"
second_title: "Aspose.Words para Java"
description: "Especifica cómo el documento se divide en partes al guardarlo en el formato SaveFormat.HTML SaveFormat.EPUB o SaveFormat.AZW_3 en Java."
type: docs
weight: 174
url: /es/java/com.aspose.words/documentsplitcriteria/
---

**Inheritance:**
java.lang.Object
```
public class DocumentSplitCriteria
```

Especifica cómo el documento se divide en partes al guardarlo en el formato [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB) o [SaveFormat.AZW\_3](../../com.aspose.words/saveformat/\#AZW-3).

 **Remarks:** 

[DocumentSplitCriteria](../../com.aspose.words/documentsplitcriteria/) is a set of flags which can be combined. For instance you can split the document at page breaks and heading paragraphs in the same export operation.

Los diferentes criterios pueden superponerse parcialmente. Por ejemplo, el estilo **Heading 1** suele recibir la propiedad [ParagraphFormat.getPageBreakBefore()](../../com.aspose.words/paragraphformat/\#getPageBreakBefore) / [ParagraphFormat.setPageBreakBefore(boolean)](../../com.aspose.words/paragraphformat/\#setPageBreakBefore-boolean) de modo que entra en dos criterios: [PAGE\_BREAK](../../com.aspose.words/documentsplitcriteria/\#PAGE-BREAK) y [HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria/\#HEADING-PARAGRAPH). Algunas rupturas de sección pueden provocar saltos de página, etc. En casos típicos, especificar solo una bandera es la opción más práctica.

 **Examples:** 

Muestra cómo usar una codificación específica al guardar un documento en .epub.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [COLUMN_BREAK](#COLUMN-BREAK) | El documento se divide en partes en los saltos de columna. |
| [HEADING_PARAGRAPH](#HEADING-PARAGRAPH) | El documento se divide en partes en un párrafo formateado con un estilo de encabezado **Heading 1**, **Heading 2**, etc. |
| [NONE](#NONE) | El documento no se divide. |
| [PAGE_BREAK](#PAGE-BREAK) | El documento se divide en partes en saltos de página explícitos. |
| [SECTION_BREAK](#SECTION-BREAK) | El documento se divide en partes en una ruptura de sección de cualquier tipo. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
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


El documento se divide en partes en los saltos de columna. Un salto de columna puede especificarse mediante un carácter [ControlChar.COLUMN\_BREAK](../../com.aspose.words/controlchar/\#COLUMN-BREAK) o una ruptura de sección que indique el inicio de una nueva sección en una nueva columna.

### HEADING_PARAGRAPH {#HEADING-PARAGRAPH}
```
public static int HEADING_PARAGRAPH
```


El documento se divide en partes en un párrafo formateado con un estilo de encabezado **Heading 1**, **Heading 2**, etc. Úselo junto con [HtmlSaveOptions.getDocumentSplitHeadingLevel()](../../com.aspose.words/htmlsaveoptions/\#getDocumentSplitHeadingLevel) / [HtmlSaveOptions.setDocumentSplitHeadingLevel(int)](../../com.aspose.words/htmlsaveoptions/\#setDocumentSplitHeadingLevel-int) para especificar los niveles de encabezado (del 1 al nivel especificado) en los que dividir.

### NONE {#NONE}
```
public static int NONE
```


El documento no se divide.

### PAGE_BREAK {#PAGE-BREAK}
```
public static int PAGE_BREAK
```


El documento se divide en partes en saltos de página explícitos. Un salto de página puede especificarse mediante un carácter [ControlChar.PAGE\_BREAK](../../com.aspose.words/controlchar/\#PAGE-BREAK), una ruptura de sección que indique el inicio de una nueva sección en una nueva página, o un párrafo que tenga su propiedad [ParagraphFormat.getPageBreakBefore()](../../com.aspose.words/paragraphformat/\#getPageBreakBefore) / [ParagraphFormat.setPageBreakBefore(boolean)](../../com.aspose.words/paragraphformat/\#setPageBreakBefore-boolean) establecida en true.

### SECTION_BREAK {#SECTION-BREAK}
```
public static int SECTION_BREAK
```


El documento se divide en partes en una ruptura de sección de cualquier tipo.

### length {#length}
```
public static int length
```


### fromName(String documentSplitCriteriaName) {#fromName-java.lang.String}
```
public static int fromName(String documentSplitCriteriaName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| documentSplitCriteriaName | java.lang.String |  |

**Returns:**
int
### fromNames(Set documentSplitCriteriaNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set documentSplitCriteriaNames)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| documentSplitCriteriaNames | java.util.Set |  |

**Returns:**
int
### getName(int documentSplitCriteria) {#getName-int}
```
public static String getName(int documentSplitCriteria)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| documentSplitCriteria | int |  |

**Returns:**
java.lang.String
### getNames(int documentSplitCriteria) {#getNames-int}
```
public static Set getNames(int documentSplitCriteria)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| documentSplitCriteria | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
