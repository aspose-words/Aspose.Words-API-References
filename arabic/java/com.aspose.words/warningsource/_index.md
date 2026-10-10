---
title: "WarningSource"
linktitle: "WarningSource"
second_title: "Aspose.Words لـ Java"
description: "يحدد الوحدة التي تُنتج تحذيراً أثناء تحميل أو حفظ المستند في Java."
type: docs
weight: 719
url: /ar/java/com.aspose.words/warningsource/
---

**Inheritance:**
java.lang.Object
```
public class WarningSource
```

يحدد الوحدة التي تُنتج تحذيرًا أثناء تحميل المستند أو حفظه.

 **Examples:** 

يوضح كيفية التعامل مع مصدر التحذير.

```

 Document doc = new Document(getMyDir() + "Emphases markdown warning.docx");

 WarningInfoCollection warnings = new WarningInfoCollection();
 doc.setWarningCallback(warnings);
 doc.save(getArtifactsDir() + "DocumentBuilder.EmphasesWarningSourceMarkdown.md");

 for (WarningInfo warningInfo : warnings) {
     if (warningInfo.getSource() == WarningSource.MARKDOWN)
         Assert.assertEquals("The (*, 0:11) cannot be properly written into Markdown.", warningInfo.getDescription());
 }
 
```

يوضح كيفية الحصول على معلومات إضافية حول استبدال الخط.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 WarningInfoCollection callback = new WarningInfoCollection();
 doc.setWarningCallback(callback);

 FontSettings fontSettings = new FontSettings();
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
 fontSettings.setFontsFolder(getFontsDir(), false);
 fontSettings.getSubstitutionSettings().getTableSubstitution().addSubstitutes("Arial", "Arvo", "Slab");

 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.SubstitutionWarnings.pdf");

 FontSubstitutionWarningInfo warningInfo = (FontSubstitutionWarningInfo)callback.get(0);
 Assert.assertEquals(WarningSource.LAYOUT, warningInfo.getSource());
 Assert.assertEquals(WarningType.FONT_SUBSTITUTION, warningInfo.getWarningType());
 Assert.assertEquals(FontSubstitutionReason.TABLE_SUBSTITUTION_RULE, warningInfo.getReason());
 Assert.assertEquals("Font \'Arial\' has not been found. Using \'Arvo\' font instead. Reason: table substitution.", warningInfo.getDescription());
 Assert.assertTrue(warningInfo.getRequestedBold());
 Assert.assertFalse(warningInfo.getRequestedItalic());
 Assert.assertEquals("Arial", warningInfo.getRequestedFamilyName());
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [CHM](#CHM) | الوحدة التي تقرأ ملفات CHM. |
| [DOC](#DOC) | الوحدة التي تقرأ/تكتب ملفات DOC الثنائية. |
| [DOCLING](#DOCLING) | الوحدة التي تكتب ملفات Docling JSON. |
| [DOCX](#DOCX) | الوحدة التي تقرأ/تكتب ملفات DOCX. |
| [DRAWING_ML](#DRAWING-ML) | الوحدة التي تُظهر أشكال DrawingML. |
| [EPUB](#EPUB) | الوحدة التي تقرأ/تكتب ملفات EPUB. |
| [FONT](#FONT) | الوحدة التي تقرأ ملفات الخطوط. |
| [HTML](#HTML) | الوحدة التي تقرأ/تكتب ملفات HTML/MHTML. |
| [IMAGE](#IMAGE) | الوحدة التي تُظهر الصور. |
| [LAYOUT](#LAYOUT) | الوحدة التي تُنشئ تخطيط المستند. |
| [MARKDOWN](#MARKDOWN) | الوحدة التي تقرأ/تكتب ملفات Markdown. |
| [MATH_ML](#MATH-ML) | الوحدة التي تقرأ ملفات W3C MathML. |
| [METAFILE](#METAFILE) | الوحدة التي تُظهر ملفات الميتا. |
| [NRX](#NRX) | الوحدات المشتركة التي تُشارك بين وحدات القارئ/الكاتب DOCX/WML. |
| [ODT](#ODT) | الوحدة التي تقرأ/تكتب ملفات ODT. |
| [OFFICE_MATH](#OFFICE-MATH) | الوحدة التي تُظهر OfficeMath. |
| [PDF](#PDF) | الوحدة التي تُظهر PDF. |
| [RTF](#RTF) | الوحدة التي تقرأ/تكتب ملفات RTF. |
| [SHAPES](#SHAPES) | الوحدة التي تُظهر الأشكال العادية. |
| [SVG](#SVG) | الوحدة التي تقرأ ملفات SVG. |
| [SVM](#SVM) | الوحدة التي تقرأ ملفات Svm. |
| [TEXT](#TEXT) | الوحدة التي تقرأ/تكتب ملفات النص العادي. |
| [UNKNOWN](#UNKNOWN) | مصدر التحذير غير محدد. |
| [VALIDATOR](#VALIDATOR) | الوحدة التي تتحقق من اتساق النموذج وصحته. |
| [WORD_ML](#WORD-ML) | الوحدة التي تقرأ/تكتب ملفات WML. |
| [XAML](#XAML) | الوحدة التي تقرأ/تكتب ملفات Xaml. |
| [XLSX](#XLSX) | الوحدة التي تكتب ملفات XLSX. |
| [XML](#XML) | الوحدة التي تقرأ ملفات XML. |
| [XPS](#XPS) | الوحدة التي تعرض XPS. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String warningSourceName)](#fromName-java.lang.String) |  |
| [getName(int warningSource)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int warningSource)](#toString-int) |  |
### CHM {#CHM}
```
public static int CHM
```


الوحدة التي تقرأ ملفات CHM.

### DOC {#DOC}
```
public static int DOC
```


الوحدة التي تقرأ/تكتب ملفات DOC الثنائية.

### DOCLING {#DOCLING}
```
public static int DOCLING
```


الوحدة التي تكتب ملفات Docling JSON.

### DOCX {#DOCX}
```
public static int DOCX
```


الوحدة التي تقرأ/تكتب ملفات DOCX.

### DRAWING_ML {#DRAWING-ML}
```
public static int DRAWING_ML
```


الوحدة التي تُظهر أشكال DrawingML.

### EPUB {#EPUB}
```
public static int EPUB
```


الوحدة التي تقرأ/تكتب ملفات EPUB.

### FONT {#FONT}
```
public static int FONT
```


الوحدة التي تقرأ ملفات الخطوط.

### HTML {#HTML}
```
public static int HTML
```


الوحدة التي تقرأ/تكتب ملفات HTML/MHTML.

### IMAGE {#IMAGE}
```
public static int IMAGE
```


الوحدة التي تُظهر الصور.

### LAYOUT {#LAYOUT}
```
public static int LAYOUT
```


الوحدة التي تُنشئ تخطيط المستند.

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


الوحدة التي تقرأ/تكتب ملفات Markdown.

### MATH_ML {#MATH-ML}
```
public static int MATH_ML
```


الوحدة التي تقرأ ملفات W3C MathML.

### METAFILE {#METAFILE}
```
public static int METAFILE
```


الوحدة التي تُظهر ملفات الميتا.

### NRX {#NRX}
```
public static int NRX
```


الوحدات المشتركة التي تُشارك بين وحدات القارئ/الكاتب DOCX/WML.

### ODT {#ODT}
```
public static int ODT
```


الوحدة التي تقرأ/تكتب ملفات ODT.

### OFFICE_MATH {#OFFICE-MATH}
```
public static int OFFICE_MATH
```


الوحدة التي تُظهر OfficeMath.

### PDF {#PDF}
```
public static int PDF
```


الوحدة التي تُظهر PDF.

### RTF {#RTF}
```
public static int RTF
```


الوحدة التي تقرأ/تكتب ملفات RTF.

### SHAPES {#SHAPES}
```
public static int SHAPES
```


الوحدة التي تُظهر الأشكال العادية.

### SVG {#SVG}
```
public static int SVG
```


الوحدة التي تقرأ ملفات SVG.

### SVM {#SVM}
```
public static int SVM
```


الوحدة التي تقرأ ملفات Svm.

### TEXT {#TEXT}
```
public static int TEXT
```


الوحدة التي تقرأ/تكتب ملفات النص العادي.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


مصدر التحذير غير محدد.

### VALIDATOR {#VALIDATOR}
```
public static int VALIDATOR
```


الوحدة التي تتحقق من اتساق النموذج وصحته.

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


الوحدة التي تقرأ/تكتب ملفات WML.

### XAML {#XAML}
```
public static int XAML
```


الوحدة التي تقرأ/تكتب ملفات Xaml.

### XLSX {#XLSX}
```
public static int XLSX
```


الوحدة التي تكتب ملفات XLSX.

### XML {#XML}
```
public static int XML
```


الوحدة التي تقرأ ملفات XML.

### XPS {#XPS}
```
public static int XPS
```


الوحدة التي تعرض XPS.

### length {#length}
```
public static int length
```


### fromName(String warningSourceName) {#fromName-java.lang.String}
```
public static int fromName(String warningSourceName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| warningSourceName | java.lang.String |  |

**Returns:**
int
### getName(int warningSource) {#getName-int}
```
public static String getName(int warningSource)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| warningSource | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int warningSource) {#toString-int}
```
public static String toString(int warningSource)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| warningSource | int |  |

**Returns:**
java.lang.String
