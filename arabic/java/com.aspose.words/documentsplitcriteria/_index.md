---
title: "DocumentSplitCriteria"
linktitle: "DocumentSplitCriteria"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية تقسيم المستند إلى أجزاء عند الحفظ بتنسيق SaveFormat.HTML أو SaveFormat.EPUB أو SaveFormat.AZW_3 في جافا."
type: docs
weight: 174
url: /ar/java/com.aspose.words/documentsplitcriteria/
---

**Inheritance:**
java.lang.Object
```
public class DocumentSplitCriteria
```

يحدد كيفية تقسيم المستند إلى أجزاء عند الحفظ بتنسيق [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB) أو [SaveFormat.AZW\_3](../../com.aspose.words/saveformat/\#AZW-3).

 **Remarks:** 

[DocumentSplitCriteria](../../com.aspose.words/documentsplitcriteria/) is a set of flags which can be combined. For instance you can split the document at page breaks and heading paragraphs in the same export operation.

يمكن أن تتداخل المعايير المختلفة جزئياً. على سبيل المثال، نمط **Heading 1** يُعطى غالباً الخاصية [ParagraphFormat.getPageBreakBefore()](../../com.aspose.words/paragraphformat/\#getPageBreakBefore) / [ParagraphFormat.setPageBreakBefore(boolean)](../../com.aspose.words/paragraphformat/\#setPageBreakBefore-boolean) بحيث يندرج تحت معيارين: [PAGE\_BREAK](../../com.aspose.words/documentsplitcriteria/\#PAGE-BREAK) و [HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria/\#HEADING-PARAGRAPH). بعض فواصل الأقسام يمكن أن تتسبب في فواصل صفحات وما إلى ذلك. في الحالات النموذجية، تحديد علم واحد فقط هو الخيار الأكثر عملية.

 **Examples:** 

يوضح كيفية استخدام ترميز محدد عند حفظ المستند بصيغة .epub.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [COLUMN_BREAK](#COLUMN-BREAK) | يتم تقسيم المستند إلى أجزاء عند فواصل الأعمدة. |
| [HEADING_PARAGRAPH](#HEADING-PARAGRAPH) | يتم تقسيم المستند إلى أجزاء عند فقرة مُنسقة باستخدام نمط عنوان **Heading 1**، **Heading 2** إلخ. |
| [NONE](#NONE) | المستند غير مقسّم. |
| [PAGE_BREAK](#PAGE-BREAK) | يتم تقسيم المستند إلى أجزاء عند فواصل صفحات صريحة. |
| [SECTION_BREAK](#SECTION-BREAK) | يتم تقسيم المستند إلى أجزاء عند فاصل قسم من أي نوع. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
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


يتم تقسيم المستند إلى أجزاء عند فواصل الأعمدة. يمكن تحديد فاصل العمود بواسطة حرف [ControlChar.COLUMN\_BREAK](../../com.aspose.words/controlchar/\#COLUMN-BREAK) أو فاصل قسم يحدد بدء قسم جديد في عمود جديد.

### HEADING_PARAGRAPH {#HEADING-PARAGRAPH}
```
public static int HEADING_PARAGRAPH
```


يتم تقسيم المستند إلى أجزاء عند فقرة مُنسقة باستخدام نمط عنوان **Heading 1**، **Heading 2** إلخ. استخدم ذلك مع [HtmlSaveOptions.getDocumentSplitHeadingLevel()](../../com.aspose.words/htmlsaveoptions/\#getDocumentSplitHeadingLevel) / [HtmlSaveOptions.setDocumentSplitHeadingLevel(int)](../../com.aspose.words/htmlsaveoptions/\#setDocumentSplitHeadingLevel-int) لتحديد مستويات العناوين (من 1 إلى المستوى المحدد) التي يتم عندها التقسيم.

### NONE {#NONE}
```
public static int NONE
```


المستند غير مقسّم.

### PAGE_BREAK {#PAGE-BREAK}
```
public static int PAGE_BREAK
```


يتم تقسيم المستند إلى أجزاء عند فواصل صفحات صريحة. يمكن تحديد فاصل الصفحة بواسطة حرف [ControlChar.PAGE\_BREAK](../../com.aspose.words/controlchar/\#PAGE-BREAK) أو فاصل قسم يحدد بدء قسم جديد في صفحة جديدة، أو فقرة لديها الخاصية [ParagraphFormat.getPageBreakBefore()](../../com.aspose.words/paragraphformat/\#getPageBreakBefore) / [ParagraphFormat.setPageBreakBefore(boolean)](../../com.aspose.words/paragraphformat/\#setPageBreakBefore-boolean) مضبوطة على true.

### SECTION_BREAK {#SECTION-BREAK}
```
public static int SECTION_BREAK
```


يتم تقسيم المستند إلى أجزاء عند فاصل قسم من أي نوع.

### length {#length}
```
public static int length
```


### fromName(String documentSplitCriteriaName) {#fromName-java.lang.String}
```
public static int fromName(String documentSplitCriteriaName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| documentSplitCriteriaName | java.lang.String |  |

**Returns:**
int
### fromNames(Set documentSplitCriteriaNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set documentSplitCriteriaNames)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| documentSplitCriteriaNames | java.util.Set |  |

**Returns:**
int
### getName(int documentSplitCriteria) {#getName-int}
```
public static String getName(int documentSplitCriteria)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| documentSplitCriteria | int |  |

**Returns:**
java.lang.String
### getNames(int documentSplitCriteria) {#getNames-int}
```
public static Set getNames(int documentSplitCriteria)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| documentSplitCriteria | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
