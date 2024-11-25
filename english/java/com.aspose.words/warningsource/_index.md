---
title: WarningSource
linktitle: WarningSource
second_title: Aspose.Words for Java
description: Specifies the module that produces a warning during document loading or saving in Java.
type: docs
weight: 676
url: /java/com.aspose.words/warningsource/
---

**Inheritance:**
java.lang.Object
```
public class WarningSource
```

Specifies the module that produces a warning during document loading or saving.

 **Examples:** 

Shows how to work with the warning source.

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
## Fields

| Field | Description |
| --- | --- |
| [CHM](#CHM) | Module that reads CHM files. |
| [DOC](#DOC) | Module that reads/writes binary DOC files. |
| [DOCX](#DOCX) | Module that reads/writes DOCX files. |
| [DRAWING_ML](#DRAWING-ML) | Module that renders DrawingML shapes. |
| [EPUB](#EPUB) | Module that reads/writes EPUB files. |
| [FONT](#FONT) | Module that reads font files. |
| [HTML](#HTML) | Module that reads/writes HTML/MHTML files. |
| [IMAGE](#IMAGE) | Module that renders images. |
| [LAYOUT](#LAYOUT) | Module that builds a document layout. |
| [MARKDOWN](#MARKDOWN) | Module that reads/writes Markdown files. |
| [MATH_ML](#MATH-ML) | Module that reads W3C MathML files. |
| [METAFILE](#METAFILE) | Module that renders metafiles. |
| [NRX](#NRX) | Common modules that are shared between DOCX/WML reader/writer modules. |
| [ODT](#ODT) | Module that reads/writes ODT files. |
| [OFFICE_MATH](#OFFICE-MATH) | Module that renders OfficeMath. |
| [PDF](#PDF) | Module that renders PDF. |
| [RTF](#RTF) | Module that reads/writes RTF files. |
| [SHAPES](#SHAPES) | Module that renders ordinary shapes. |
| [SVG](#SVG) | Module that reads SVG files. |
| [SVM](#SVM) | Module that reads Svm files. |
| [TEXT](#TEXT) | Module that reads/writes plaintext files. |
| [UNKNOWN](#UNKNOWN) | The warning source is not specified. |
| [VALIDATOR](#VALIDATOR) | Module that verifies model consistency and validity. |
| [WORD_ML](#WORD-ML) | Module that reads/writes WML files. |
| [XAML](#XAML) | Module that reads/writes Xaml files. |
| [XLSX](#XLSX) | Module that writes XLSX files. |
| [XML](#XML) | Module that reads XML files. |
| [XPS](#XPS) | Module that renders XPS. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String warningSourceName)](#fromName-java.lang.String) |  |
| [getName(int warningSource)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int warningSource)](#toString-int) |  |
### CHM {#CHM}
```
public static int CHM
```


Module that reads CHM files.

### DOC {#DOC}
```
public static int DOC
```


Module that reads/writes binary DOC files.

### DOCX {#DOCX}
```
public static int DOCX
```


Module that reads/writes DOCX files.

### DRAWING_ML {#DRAWING-ML}
```
public static int DRAWING_ML
```


Module that renders DrawingML shapes.

### EPUB {#EPUB}
```
public static int EPUB
```


Module that reads/writes EPUB files.

### FONT {#FONT}
```
public static int FONT
```


Module that reads font files.

### HTML {#HTML}
```
public static int HTML
```


Module that reads/writes HTML/MHTML files.

### IMAGE {#IMAGE}
```
public static int IMAGE
```


Module that renders images.

### LAYOUT {#LAYOUT}
```
public static int LAYOUT
```


Module that builds a document layout.

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


Module that reads/writes Markdown files.

### MATH_ML {#MATH-ML}
```
public static int MATH_ML
```


Module that reads W3C MathML files.

### METAFILE {#METAFILE}
```
public static int METAFILE
```


Module that renders metafiles.

### NRX {#NRX}
```
public static int NRX
```


Common modules that are shared between DOCX/WML reader/writer modules.

### ODT {#ODT}
```
public static int ODT
```


Module that reads/writes ODT files.

### OFFICE_MATH {#OFFICE-MATH}
```
public static int OFFICE_MATH
```


Module that renders OfficeMath.

### PDF {#PDF}
```
public static int PDF
```


Module that renders PDF.

### RTF {#RTF}
```
public static int RTF
```


Module that reads/writes RTF files.

### SHAPES {#SHAPES}
```
public static int SHAPES
```


Module that renders ordinary shapes.

### SVG {#SVG}
```
public static int SVG
```


Module that reads SVG files.

### SVM {#SVM}
```
public static int SVM
```


Module that reads Svm files.

### TEXT {#TEXT}
```
public static int TEXT
```


Module that reads/writes plaintext files.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


The warning source is not specified.

### VALIDATOR {#VALIDATOR}
```
public static int VALIDATOR
```


Module that verifies model consistency and validity.

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


Module that reads/writes WML files.

### XAML {#XAML}
```
public static int XAML
```


Module that reads/writes Xaml files.

### XLSX {#XLSX}
```
public static int XLSX
```


Module that writes XLSX files.

### XML {#XML}
```
public static int XML
```


Module that reads XML files.

### XPS {#XPS}
```
public static int XPS
```


Module that renders XPS.

### length {#length}
```
public static int length
```


### fromName(String warningSourceName) {#fromName-java.lang.String}
```
public static int fromName(String warningSourceName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| warningSourceName | java.lang.String |  |

**Returns:**
int
### getName(int warningSource) {#getName-int}
```
public static String getName(int warningSource)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| warningSource | int |  |

**Returns:**
java.lang.String
