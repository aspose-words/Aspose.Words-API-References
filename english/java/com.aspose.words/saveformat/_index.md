---
title: SaveFormat
linktitle: SaveFormat
second_title: Aspose.Words for Java
description: Indicates the format in which the document is saved in Java.
type: docs
weight: 560
url: /java/com.aspose.words/saveformat/
---

**Inheritance:**
java.lang.Object
```
public class SaveFormat
```

Indicates the format in which the document is saved.

 **Examples:** 

Shows how to convert from DOCX to HTML format.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 doc.save(getArtifactsDir() + "Document.ConvertToHtml.html", SaveFormat.HTML);
 
```

**M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.SaveFormat)**
## Fields

| Field | Description |
| --- | --- |
| [AZW_3](#AZW-3) | Saves the document in the AZW3 format. |
| [BMP](#BMP) | Renders a page of the document and saves it as a BMP file. |
| [DOC](#DOC) | Saves the document in the Microsoft Word 97 - 2007 Document format. |
| [DOCM](#DOCM) | Saves the document as an Office Open XML WordprocessingML Macro-Enabled Document. |
| [DOCX](#DOCX) | Saves the document as an Office Open XML WordprocessingML Document (macro-free). |
| [DOT](#DOT) | Saves the document in the Microsoft Word 97 - 2007 Template format. |
| [DOTM](#DOTM) | Saves the document as an Office Open XML WordprocessingML Macro-Enabled Template. |
| [DOTX](#DOTX) | Saves the document as an Office Open XML WordprocessingML Template (macro-free). |
| [EMF](#EMF) | Renders a page of the document and saves it as a vector EMF (Enhanced Meta File) file. |
| [EPS](#EPS) | Renders a page of the document and saves it as an EPS file. |
| [EPUB](#EPUB) | Saves the document in the EPUB format. |
| [FLAT_OPC](#FLAT-OPC) | Saves the document as an Office Open XML WordprocessingML stored in a flat XML file instead of a ZIP package. |
| [FLAT_OPC_MACRO_ENABLED](#FLAT-OPC-MACRO-ENABLED) | Saves the document as an Office Open XML WordprocessingML Macro-Enabled Document stored in a flat XML file instead of a ZIP package. |
| [FLAT_OPC_TEMPLATE](#FLAT-OPC-TEMPLATE) | Saves the document as an Office Open XML WordprocessingML Template (macro-free) stored in a flat XML file instead of a ZIP package. |
| [FLAT_OPC_TEMPLATE_MACRO_ENABLED](#FLAT-OPC-TEMPLATE-MACRO-ENABLED) | Saves the document as an Office Open XML WordprocessingML Macro-Enabled Template stored in a flat XML file instead of a ZIP package. |
| [GIF](#GIF) | Renders a page of the document and saves it as a GIF file. |
| [HTML](#HTML) | Saves the document in the HTML format. |
| [HTML_FIXED](#HTML-FIXED) | Saves the document in the HTML format using absolutely positioned elements |
| [JPEG](#JPEG) | Renders a page of the document and saves it as a JPEG file. |
| [MARKDOWN](#MARKDOWN) | Saves the document in the Markdown format. |
| [MHTML](#MHTML) | Saves the document in the MHTML (Web archive) format. |
| [MOBI](#MOBI) | Saves the document in the MOBI format. |
| [ODT](#ODT) | Saves the document as an ODF Text Document. |
| [OPEN_XPS](#OPEN-XPS) | Saves the document in the OpenXPS (Ecma-388) format. |
| [OTT](#OTT) | Saves the document as an ODF Text Document Template. |
| [PCL](#PCL) | Saves the document in the PCL (Printer Control Language) format. |
| [PDF](#PDF) | Saves the document as PDF (Adobe Portable Document) format. |
| [PNG](#PNG) | Renders a page of the document and saves it as a PNG file. |
| [PS](#PS) | Saves the document in the PS (PostScript) format. |
| [RTF](#RTF) | Saves the document in the RTF format. |
| [SVG](#SVG) | Saves the document in the Svg (Scalable Vector Graphics) format. |
| [TEXT](#TEXT) | Saves the document in the plain text format. |
| [TIFF](#TIFF) | Renders a page or pages of the document and saves them into a single or multipage TIFF file. |
| [UNKNOWN](#UNKNOWN) | Default, invalid value for file format. |
| [WEB_P](#WEB-P) | Renders a page of the document and saves it as a WebP file. |
| [WORD_ML](#WORD-ML) | Saves the document in the Microsoft Word 2003 WordprocessingML format. |
| [XAML_FIXED](#XAML-FIXED) | Saves the document in the Extensible Application Markup Language (XAML) format as a fixed document. |
| [XAML_FLOW](#XAML-FLOW) | **Beta.** Saves the document in the Extensible Application Markup Language (XAML) format as a flow document. |
| [XAML_FLOW_PACK](#XAML-FLOW-PACK) | **Beta.** Saves the document in the Extensible Application Markup Language (XAML) package format as a flow document. |
| [XLSX](#XLSX) | Saves the document as an Office Open XML SpreadsheetML Document (macro-free). |
| [XPS](#XPS) | Saves the document in the XPS (XML Paper Specification) format. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String saveFormatName)](#fromName-java.lang.String) |  |
| [getName(int saveFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int saveFormat)](#toString-int) |  |
### AZW_3 {#AZW-3}
```
public static int AZW_3
```


Saves the document in the AZW3 format.

### BMP {#BMP}
```
public static int BMP
```


Renders a page of the document and saves it as a BMP file.

### DOC {#DOC}
```
public static int DOC
```


Saves the document in the Microsoft Word 97 - 2007 Document format.

### DOCM {#DOCM}
```
public static int DOCM
```


Saves the document as an Office Open XML WordprocessingML Macro-Enabled Document.

### DOCX {#DOCX}
```
public static int DOCX
```


Saves the document as an Office Open XML WordprocessingML Document (macro-free).

### DOT {#DOT}
```
public static int DOT
```


Saves the document in the Microsoft Word 97 - 2007 Template format.

### DOTM {#DOTM}
```
public static int DOTM
```


Saves the document as an Office Open XML WordprocessingML Macro-Enabled Template.

### DOTX {#DOTX}
```
public static int DOTX
```


Saves the document as an Office Open XML WordprocessingML Template (macro-free).

### EMF {#EMF}
```
public static int EMF
```


Renders a page of the document and saves it as a vector EMF (Enhanced Meta File) file.

### EPS {#EPS}
```
public static int EPS
```


Renders a page of the document and saves it as an EPS file.

### EPUB {#EPUB}
```
public static int EPUB
```


Saves the document in the EPUB format.

### FLAT_OPC {#FLAT-OPC}
```
public static int FLAT_OPC
```


Saves the document as an Office Open XML WordprocessingML stored in a flat XML file instead of a ZIP package.

### FLAT_OPC_MACRO_ENABLED {#FLAT-OPC-MACRO-ENABLED}
```
public static int FLAT_OPC_MACRO_ENABLED
```


Saves the document as an Office Open XML WordprocessingML Macro-Enabled Document stored in a flat XML file instead of a ZIP package.

### FLAT_OPC_TEMPLATE {#FLAT-OPC-TEMPLATE}
```
public static int FLAT_OPC_TEMPLATE
```


Saves the document as an Office Open XML WordprocessingML Template (macro-free) stored in a flat XML file instead of a ZIP package.

### FLAT_OPC_TEMPLATE_MACRO_ENABLED {#FLAT-OPC-TEMPLATE-MACRO-ENABLED}
```
public static int FLAT_OPC_TEMPLATE_MACRO_ENABLED
```


Saves the document as an Office Open XML WordprocessingML Macro-Enabled Template stored in a flat XML file instead of a ZIP package.

### GIF {#GIF}
```
public static int GIF
```


Renders a page of the document and saves it as a GIF file.

### HTML {#HTML}
```
public static int HTML
```


Saves the document in the HTML format.

### HTML_FIXED {#HTML-FIXED}
```
public static int HTML_FIXED
```


Saves the document in the HTML format using absolutely positioned elements

### JPEG {#JPEG}
```
public static int JPEG
```


Renders a page of the document and saves it as a JPEG file.

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


Saves the document in the Markdown format.

### MHTML {#MHTML}
```
public static int MHTML
```


Saves the document in the MHTML (Web archive) format.

### MOBI {#MOBI}
```
public static int MOBI
```


Saves the document in the MOBI format.

### ODT {#ODT}
```
public static int ODT
```


Saves the document as an ODF Text Document.

### OPEN_XPS {#OPEN-XPS}
```
public static int OPEN_XPS
```


Saves the document in the OpenXPS (Ecma-388) format.

### OTT {#OTT}
```
public static int OTT
```


Saves the document as an ODF Text Document Template.

### PCL {#PCL}
```
public static int PCL
```


Saves the document in the PCL (Printer Control Language) format.

### PDF {#PDF}
```
public static int PDF
```


Saves the document as PDF (Adobe Portable Document) format.

### PNG {#PNG}
```
public static int PNG
```


Renders a page of the document and saves it as a PNG file.

### PS {#PS}
```
public static int PS
```


Saves the document in the PS (PostScript) format.

### RTF {#RTF}
```
public static int RTF
```


Saves the document in the RTF format. All characters above 7-bits are escaped as hexadecimal or Unicode characters.

### SVG {#SVG}
```
public static int SVG
```


Saves the document in the Svg (Scalable Vector Graphics) format.

### TEXT {#TEXT}
```
public static int TEXT
```


Saves the document in the plain text format.

### TIFF {#TIFF}
```
public static int TIFF
```


Renders a page or pages of the document and saves them into a single or multipage TIFF file.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Default, invalid value for file format.

### WEB_P {#WEB-P}
```
public static int WEB_P
```


Renders a page of the document and saves it as a WebP file.

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


Saves the document in the Microsoft Word 2003 WordprocessingML format.

### XAML_FIXED {#XAML-FIXED}
```
public static int XAML_FIXED
```


Saves the document in the Extensible Application Markup Language (XAML) format as a fixed document.

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


Saves the document as an Office Open XML SpreadsheetML Document (macro-free).

### XPS {#XPS}
```
public static int XPS
```


Saves the document in the XPS (XML Paper Specification) format.

### length {#length}
```
public static int length
```


### fromName(String saveFormatName) {#fromName-java.lang.String}
```
public static int fromName(String saveFormatName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormatName | java.lang.String |  |

**Returns:**
int
### getName(int saveFormat) {#getName-int}
```
public static String getName(int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
