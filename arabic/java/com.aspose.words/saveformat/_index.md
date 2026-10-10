---
title: "SaveFormat"
linktitle: "SaveFormat"
second_title: "Aspose.Words لـ Java"
description: "يشير إلى التنسيق الذي يتم حفظ المستند به في Java."
type: docs
weight: 595
url: /ar/java/com.aspose.words/saveformat/
---

**Inheritance:**
java.lang.Object
```
public class SaveFormat
```

يشير إلى التنسيق الذي يتم حفظ المستند به.

 **Examples:** 

يظهر كيفية التحويل من تنسيق DOCX إلى HTML.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 doc.save(getArtifactsDir() + "Document.ConvertToHtml.html", SaveFormat.HTML);
 
```

**M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.SaveFormat)**
## الحقول

| حقل | الوصف |
| --- | --- |
| [AZW_3](#AZW-3) | يحفظ المستند بتنسيق AZW3. |
| [BMP](#BMP) | يصوّر صفحة من المستند ويحفظها كملف BMP. |
| [DOC](#DOC) | يحفظ المستند بتنسيق Microsoft Word 97 - 2007. |
| [DOCLING](#DOCLING) | يحفظ المستند بتنسيق Docling JSON. |
| [DOCM](#DOCM) | يحفظ المستند كمستند Office Open XML WordprocessingML مع تمكين الماكرو. |
| [DOCX](#DOCX) | يحفظ المستند كمستند Office Open XML WordprocessingML (بدون ماكرو). |
| [DOT](#DOT) | يحفظ المستند بتنسيق قالب Microsoft Word 97 - 2007. |
| [DOTM](#DOTM) | يحفظ المستند كقالب Office Open XML WordprocessingML مع تمكين الماكرو. |
| [DOTX](#DOTX) | يحفظ المستند كقالب Office Open XML WordprocessingML (بدون ماكرو). |
| [EMF](#EMF) | يصوّر صفحة من المستند ويحفظها كملف EMF (Enhanced Meta File) متجه. |
| [EPS](#EPS) | يصوّر صفحة من المستند ويحفظها كملف EPS. |
| [EPUB](#EPUB) | يحفظ المستند بتنسيق EPUB. |
| [FLAT_OPC](#FLAT-OPC) | يحفظ المستند كـ Office Open XML WordprocessingML مخزن في ملف XML مسطح بدلاً من حزمة ZIP. |
| [FLAT_OPC_MACRO_ENABLED](#FLAT-OPC-MACRO-ENABLED) | يحفظ المستند كـ Office Open XML WordprocessingML Macro-Enabled Document مخزن في ملف XML مسطح بدلاً من حزمة ZIP. |
| [FLAT_OPC_TEMPLATE](#FLAT-OPC-TEMPLATE) | يحفظ المستند كـ Office Open XML WordprocessingML Template (macro-free) مخزن في ملف XML مسطح بدلاً من حزمة ZIP. |
| [FLAT_OPC_TEMPLATE_MACRO_ENABLED](#FLAT-OPC-TEMPLATE-MACRO-ENABLED) | يحفظ المستند كـ Office Open XML WordprocessingML Macro-Enabled Template مخزن في ملف XML مسطح بدلاً من حزمة ZIP. |
| [GIF](#GIF) | يقوم بتصوير صفحة من المستند ويحفظها كملف GIF. |
| [HTML](#HTML) | يحفظ المستند بتنسيق HTML. |
| [HTML_FIXED](#HTML-FIXED) | يحفظ المستند بتنسيق HTML باستخدام عناصر موضوعة بشكل مطلق |
| [JPEG](#JPEG) | يقوم بتصوير صفحة من المستند ويحفظها كملف JPEG. |
| [MARKDOWN](#MARKDOWN) | يحفظ المستند بتنسيق Markdown. |
| [MHTML](#MHTML) | يحفظ المستند بتنسيق MHTML (Web archive). |
| [MOBI](#MOBI) | يحفظ المستند بتنسيق MOBI. |
| [ODT](#ODT) | يحفظ المستند كـ ODF Text Document. |
| [OPEN_XPS](#OPEN-XPS) | يحفظ المستند بتنسيق OpenXPS (Ecma-388). |
| [OTT](#OTT) | يحفظ المستند كـ ODF Text Document Template. |
| [PCL](#PCL) | يحفظ المستند بتنسيق PCL (Printer Control Language). |
| [PDF](#PDF) | يحفظ المستند بتنسيق PDF (Adobe Portable Document). |
| [PNG](#PNG) | يقوم بتصوير صفحة من المستند ويحفظها كملف PNG. |
| [PS](#PS) | يحفظ المستند بتنسيق PS (PostScript). |
| [RTF](#RTF) | يحفظ المستند بتنسيق RTF. |
| [SVG](#SVG) | يحفظ المستند بتنسيق Svg (Scalable Vector Graphics). |
| [TEXT](#TEXT) | يحفظ المستند بتنسيق النص العادي. |
| [TIFF](#TIFF) | يقوم بتصوير صفحة أو صفحات من المستند ويحفظها في ملف TIFF واحد أو متعدد الصفحات. |
| [UNKNOWN](#UNKNOWN) | القيمة الافتراضية، قيمة غير صالحة لتنسيق الملف. |
| [WEB_P](#WEB-P) | يقوم بتصوير صفحة من المستند ويحفظها كملف WebP. |
| [WORD_ML](#WORD-ML) | يحفظ المستند بتنسيق Microsoft Word 2003 WordprocessingML. |
| [XAML_FIXED](#XAML-FIXED) | يحفظ المستند بتنسيق Extensible Application Markup Language (XAML) كمستند ثابت. |
| [XAML_FLOW](#XAML-FLOW) | **Beta.** يحفظ المستند بتنسيق Extensible Application Markup Language (XAML) كمستند متدفق. |
| [XAML_FLOW_PACK](#XAML-FLOW-PACK) | **Beta.** يحفظ المستند بتنسيق حزمة Extensible Application Markup Language (XAML) كمستند متدفق. |
| [XLSX](#XLSX) | يحفظ المستند كوثيقة Office Open XML SpreadsheetML (بدون ماكرو). |
| [XPS](#XPS) | يحفظ المستند بتنسيق XPS (XML Paper Specification). |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String saveFormatName)](#fromName-java.lang.String) |  |
| [getName(int saveFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int saveFormat)](#toString-int) |  |
### AZW_3 {#AZW-3}
```
public static int AZW_3
```


يحفظ المستند بتنسيق AZW3.

### BMP {#BMP}
```
public static int BMP
```


يصوّر صفحة من المستند ويحفظها كملف BMP.

### DOC {#DOC}
```
public static int DOC
```


يحفظ المستند بتنسيق Microsoft Word 97 - 2007.

### DOCLING {#DOCLING}
```
public static int DOCLING
```


يحفظ المستند بتنسيق Docling JSON.

### DOCM {#DOCM}
```
public static int DOCM
```


يحفظ المستند كمستند Office Open XML WordprocessingML مع تمكين الماكرو.

### DOCX {#DOCX}
```
public static int DOCX
```


يحفظ المستند كمستند Office Open XML WordprocessingML (بدون ماكرو).

### DOT {#DOT}
```
public static int DOT
```


يحفظ المستند بتنسيق قالب Microsoft Word 97 - 2007.

### DOTM {#DOTM}
```
public static int DOTM
```


يحفظ المستند كقالب Office Open XML WordprocessingML مع تمكين الماكرو.

### DOTX {#DOTX}
```
public static int DOTX
```


يحفظ المستند كقالب Office Open XML WordprocessingML (بدون ماكرو).

### EMF {#EMF}
```
public static int EMF
```


يصوّر صفحة من المستند ويحفظها كملف EMF (Enhanced Meta File) متجه.

### EPS {#EPS}
```
public static int EPS
```


يصوّر صفحة من المستند ويحفظها كملف EPS.

### EPUB {#EPUB}
```
public static int EPUB
```


يحفظ المستند بتنسيق EPUB.

### FLAT_OPC {#FLAT-OPC}
```
public static int FLAT_OPC
```


يحفظ المستند كـ Office Open XML WordprocessingML مخزن في ملف XML مسطح بدلاً من حزمة ZIP.

### FLAT_OPC_MACRO_ENABLED {#FLAT-OPC-MACRO-ENABLED}
```
public static int FLAT_OPC_MACRO_ENABLED
```


يحفظ المستند كـ Office Open XML WordprocessingML Macro-Enabled Document مخزن في ملف XML مسطح بدلاً من حزمة ZIP.

### FLAT_OPC_TEMPLATE {#FLAT-OPC-TEMPLATE}
```
public static int FLAT_OPC_TEMPLATE
```


يحفظ المستند كـ Office Open XML WordprocessingML Template (macro-free) مخزن في ملف XML مسطح بدلاً من حزمة ZIP.

### FLAT_OPC_TEMPLATE_MACRO_ENABLED {#FLAT-OPC-TEMPLATE-MACRO-ENABLED}
```
public static int FLAT_OPC_TEMPLATE_MACRO_ENABLED
```


يحفظ المستند كـ Office Open XML WordprocessingML Macro-Enabled Template مخزن في ملف XML مسطح بدلاً من حزمة ZIP.

### GIF {#GIF}
```
public static int GIF
```


يقوم بتصوير صفحة من المستند ويحفظها كملف GIF.

### HTML {#HTML}
```
public static int HTML
```


يحفظ المستند بتنسيق HTML.

### HTML_FIXED {#HTML-FIXED}
```
public static int HTML_FIXED
```


يحفظ المستند بتنسيق HTML باستخدام عناصر موضوعة بشكل مطلق

### JPEG {#JPEG}
```
public static int JPEG
```


يقوم بتصوير صفحة من المستند ويحفظها كملف JPEG.

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


يحفظ المستند بتنسيق Markdown.

### MHTML {#MHTML}
```
public static int MHTML
```


يحفظ المستند بتنسيق MHTML (Web archive).

### MOBI {#MOBI}
```
public static int MOBI
```


يحفظ المستند بتنسيق MOBI.

### ODT {#ODT}
```
public static int ODT
```


يحفظ المستند كـ ODF Text Document.

### OPEN_XPS {#OPEN-XPS}
```
public static int OPEN_XPS
```


يحفظ المستند بتنسيق OpenXPS (Ecma-388).

### OTT {#OTT}
```
public static int OTT
```


يحفظ المستند كـ ODF Text Document Template.

### PCL {#PCL}
```
public static int PCL
```


يحفظ المستند بتنسيق PCL (Printer Control Language).

### PDF {#PDF}
```
public static int PDF
```


يحفظ المستند بتنسيق PDF (Adobe Portable Document).

### PNG {#PNG}
```
public static int PNG
```


يقوم بتصوير صفحة من المستند ويحفظها كملف PNG.

### PS {#PS}
```
public static int PS
```


يحفظ المستند بتنسيق PS (PostScript).

### RTF {#RTF}
```
public static int RTF
```


يحفظ المستند بتنسيق RTF. جميع الأحرف التي تتجاوز 7 بتات يتم هروبها كقيمة سداسية عشرية أو أحرف Unicode.

### SVG {#SVG}
```
public static int SVG
```


يحفظ المستند بتنسيق Svg (Scalable Vector Graphics).

### TEXT {#TEXT}
```
public static int TEXT
```


يحفظ المستند بتنسيق النص العادي.

### TIFF {#TIFF}
```
public static int TIFF
```


يقوم بتصوير صفحة أو صفحات من المستند ويحفظها في ملف TIFF واحد أو متعدد الصفحات.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


القيمة الافتراضية، قيمة غير صالحة لتنسيق الملف.

### WEB_P {#WEB-P}
```
public static int WEB_P
```


يقوم بتصوير صفحة من المستند ويحفظها كملف WebP.

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


يحفظ المستند بتنسيق Microsoft Word 2003 WordprocessingML.

### XAML_FIXED {#XAML-FIXED}
```
public static int XAML_FIXED
```


يحفظ المستند بتنسيق Extensible Application Markup Language (XAML) كمستند ثابت.

### XAML_FLOW {#XAML-FLOW}
```
public static int XAML_FLOW
```


**Beta.** Saves the document in the Extensible Application Markup Language (XAML) format as a flow document.

### XAML_FLOW_PACK {#XAML-FLOW-PACK}
```
public static int XAML_FLOW_PACK
```


**Beta.** Saves the document in the Extensible Application Markup Language (XAML) package format as a flow document.

### XLSX {#XLSX}
```
public static int XLSX
```


يحفظ المستند كوثيقة Office Open XML SpreadsheetML (بدون ماكرو).

### XPS {#XPS}
```
public static int XPS
```


يحفظ المستند بتنسيق XPS (XML Paper Specification).

### length {#length}
```
public static int length
```


### fromName(String saveFormatName) {#fromName-java.lang.String}
```
public static int fromName(String saveFormatName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| saveFormatName | java.lang.String |  |

**Returns:**
int
### getName(int saveFormat) {#getName-int}
```
public static String getName(int saveFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int saveFormat) {#toString-int}
```
public static String toString(int saveFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
