---
title: "DocumentSplitCriteria"
linktitle: "DocumentSplitCriteria"
second_title: "Aspose.Words Java için"
description: "Belirtilen belge, Java'da SaveFormat.HTML, SaveFormat.EPUB veya SaveFormat.AZW_3 formatına kaydedilirken nasıl parçalara bölündüğünü belirtir."
type: docs
weight: 174
url: /tr/java/com.aspose.words/documentsplitcriteria/
---

**Inheritance:**
java.lang.Object
```
public class DocumentSplitCriteria
```

Belgenin, [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB) veya [SaveFormat.AZW\_3](../../com.aspose.words/saveformat/\#AZW-3) formatına kaydedilirken nasıl parçalara bölündüğünü belirtir.

 **Remarks:** 

[DocumentSplitCriteria](../../com.aspose.words/documentsplitcriteria/) is a set of flags which can be combined. For instance you can split the document at page breaks and heading paragraphs in the same export operation.

Farklı kriterler kısmen çakışabilir. Örneğin, **Heading 1** stili genellikle [ParagraphFormat.getPageBreakBefore()](../../com.aspose.words/paragraphformat/\#getPageBreakBefore) / [ParagraphFormat.setPageBreakBefore(boolean)](../../com.aspose.words/paragraphformat/\#setPageBreakBefore-boolean) özelliğiyle verilir, bu yüzden iki kriter altında yer alır: [PAGE\_BREAK](../../com.aspose.words/documentsplitcriteria/\#PAGE-BREAK) ve [HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria/\#HEADING-PARAGRAPH). Bazı bölüm sonları sayfa sonlarına neden olabilir vb. Tipik durumlarda yalnızca bir bayrak belirtmek en pratik seçenektir.

 **Examples:** 

.epub formatına bir belge kaydederken belirli bir kodlamanın nasıl kullanılacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [COLUMN_BREAK](#COLUMN-BREAK) | Belge, sütun sonlarında parçalara bölünür. |
| [HEADING_PARAGRAPH](#HEADING-PARAGRAPH) | Belge, **Heading 1**, **Heading 2** vb. başlık stiliyle biçimlendirilmiş bir paragrafta parçalara bölünür. |
| [NONE](#NONE) | Belge bölünmez. |
| [PAGE_BREAK](#PAGE-BREAK) | Belge, belirgin sayfa sonlarında parçalara bölünür. |
| [SECTION_BREAK](#SECTION-BREAK) | Belge, herhangi bir türde bölüm sonunda parçalara bölünür. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
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


Belge, sütun sonlarında parçalara bölünür. Bir sütun sonu, bir [ControlChar.COLUMN\_BREAK](../../com.aspose.words/controlchar/\#COLUMN-BREAK) karakteriyle veya yeni bir sütunda yeni bölümün başlangıcını belirten bir bölüm sonu ile belirtilebilir.

### HEADING_PARAGRAPH {#HEADING-PARAGRAPH}
```
public static int HEADING_PARAGRAPH
```


Belge, **Heading 1**, **Heading 2** vb. başlık stiliyle biçimlendirilmiş bir paragrafta parçalara bölünür. Bölünecek başlık seviyelerini (1'den belirtilen seviyeye kadar) belirlemek için [HtmlSaveOptions.getDocumentSplitHeadingLevel()](../../com.aspose.words/htmlsaveoptions/\#getDocumentSplitHeadingLevel) / [HtmlSaveOptions.setDocumentSplitHeadingLevel(int)](../../com.aspose.words/htmlsaveoptions/\#setDocumentSplitHeadingLevel-int) ile birlikte kullanın.

### NONE {#NONE}
```
public static int NONE
```


Belge bölünmez.

### PAGE_BREAK {#PAGE-BREAK}
```
public static int PAGE_BREAK
```


Belge, belirgin sayfa sonlarında parçalara bölünür. Bir sayfa sonu, bir [ControlChar.PAGE\_BREAK](../../com.aspose.words/controlchar/\#PAGE-BREAK) karakteri, yeni bir sayfada yeni bölümün başlangıcını belirten bir bölüm sonu veya [ParagraphFormat.getPageBreakBefore()](../../com.aspose.words/paragraphformat/\#getPageBreakBefore) / [ParagraphFormat.setPageBreakBefore(boolean)](../../com.aspose.words/paragraphformat/\#setPageBreakBefore-boolean) özelliği true olarak ayarlanmış bir paragraf ile belirtilebilir.

### SECTION_BREAK {#SECTION-BREAK}
```
public static int SECTION_BREAK
```


Belge, herhangi bir türde bölüm sonunda parçalara bölünür.

### length {#length}
```
public static int length
```


### fromName(String documentSplitCriteriaName) {#fromName-java.lang.String}
```
public static int fromName(String documentSplitCriteriaName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| documentSplitCriteriaName | java.lang.String |  |

**Returns:**
int
### fromNames(Set documentSplitCriteriaNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set documentSplitCriteriaNames)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| documentSplitCriteriaNames | java.util.Set |  |

**Returns:**
int
### getName(int documentSplitCriteria) {#getName-int}
```
public static String getName(int documentSplitCriteria)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| documentSplitCriteria | int |  |

**Returns:**
java.lang.String
### getNames(int documentSplitCriteria) {#getNames-int}
```
public static Set getNames(int documentSplitCriteria)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| documentSplitCriteria | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
