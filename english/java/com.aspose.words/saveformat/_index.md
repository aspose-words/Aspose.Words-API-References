---
title: SaveFormat
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 499
url: /java/com.aspose.words/saveformat/
---

**Inheritance:**
java.lang.Object
```
public class SaveFormat
```

A utility class providing constants. Indicates the format in which the document is saved. **M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.SaveFormat)**
## Fields

| Field | Description |
| --- | --- |
| [UNKNOWN](#UNKNOWN) | Default, invalid value for file format. |
| [DOC](#DOC) | Saves the document in the Microsoft Word 97 - 2007 Document format. |
| [DOT](#DOT) | Saves the document in the Microsoft Word 97 - 2007 Template format. |
| [DOCX](#DOCX) | Saves the document as an Office Open XML WordprocessingML Document (macro-free). |
| [DOCM](#DOCM) | Saves the document as an Office Open XML WordprocessingML Macro-Enabled Document. |
| [DOTX](#DOTX) | Saves the document as an Office Open XML WordprocessingML Template (macro-free). |
| [DOTM](#DOTM) | Saves the document as an Office Open XML WordprocessingML Macro-Enabled Template. |
| [FLAT_OPC](#FLAT-OPC) | Saves the document as an Office Open XML WordprocessingML stored in a flat XML file instead of a ZIP package. |
| [FLAT_OPC_MACRO_ENABLED](#FLAT-OPC-MACRO-ENABLED) | Saves the document as an Office Open XML WordprocessingML Macro-Enabled Document stored in a flat XML file instead of a ZIP package. |
| [FLAT_OPC_TEMPLATE](#FLAT-OPC-TEMPLATE) | Saves the document as an Office Open XML WordprocessingML Template (macro-free) stored in a flat XML file instead of a ZIP package. |
| [FLAT_OPC_TEMPLATE_MACRO_ENABLED](#FLAT-OPC-TEMPLATE-MACRO-ENABLED) | Saves the document as an Office Open XML WordprocessingML Macro-Enabled Template stored in a flat XML file instead of a ZIP package. |
| [RTF](#RTF) | Saves the document in the RTF format. |
| [WORD_ML](#WORD-ML) | Saves the document in the Microsoft Word 2003 WordprocessingML format. |
| [PDF](#PDF) | Saves the document as PDF (Adobe Portable Document) format. |
| [XPS](#XPS) | Saves the document in the XPS (XML Paper Specification) format. |
| [XAML_FIXED](#XAML-FIXED) | Saves the document in the Extensible Application Markup Language (XAML) format as a fixed document. |
| [SVG](#SVG) | Saves the document in the Svg (Scalable Vector Graphics) format. |
| [HTML_FIXED](#HTML-FIXED) | Saves the document in the HTML format using absolutely positioned elements |
| [OPEN_XPS](#OPEN-XPS) | Saves the document in the OpenXPS (Ecma-388) format. |
| [PS](#PS) | Saves the document in the PS (PostScript) format. |
| [PCL](#PCL) | Saves the document in the PCL (Printer Control Language) format. |
| [HTML](#HTML) | Saves the document in the HTML format. |
| [MHTML](#MHTML) | Saves the document in the MHTML (Web archive) format. |
| [EPUB](#EPUB) | Saves the document in the EPUB format. |
| [AZW_3](#AZW-3) | Saves the document in the AZW3 format. |
| [ODT](#ODT) | Saves the document as an ODF Text Document. |
| [OTT](#OTT) | Saves the document as an ODF Text Document Template. |
| [TEXT](#TEXT) | Saves the document in the plain text format. |
| [XAML_FLOW](#XAML-FLOW) | **Beta.** Saves the document in the Extensible Application Markup Language (XAML) format as a flow document. |
| [XAML_FLOW_PACK](#XAML-FLOW-PACK) | **Beta.** Saves the document in the Extensible Application Markup Language (XAML) package format as a flow document. |
| [MARKDOWN](#MARKDOWN) | Saves the document in the Markdown format. |
| [TIFF](#TIFF) | Renders a page or pages of the document and saves them into a single or multipage TIFF file. |
| [PNG](#PNG) | Renders a page of the document and saves it as a PNG file. |
| [BMP](#BMP) | Renders a page of the document and saves it as a BMP file. |
| [EMF](#EMF) | Renders a page of the document and saves it as a vector EMF (Enhanced Meta File) file. |
| [JPEG](#JPEG) | Renders a page of the document and saves it as a JPEG file. |
| [GIF](#GIF) | Renders a page of the document and saves it as a GIF file. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int saveFormat)](#getName-int-) |  |
| [toString(int saveFormat)](#toString-int-) |  |
| [fromName(String saveFormatName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Default, invalid value for file format.

### DOC {#DOC}
```
public static int DOC
```


Saves the document in the Microsoft Word 97 - 2007 Document format.

### DOT {#DOT}
```
public static int DOT
```


Saves the document in the Microsoft Word 97 - 2007 Template format.

### DOCX {#DOCX}
```
public static int DOCX
```


Saves the document as an Office Open XML WordprocessingML Document (macro-free).

### DOCM {#DOCM}
```
public static int DOCM
```


Saves the document as an Office Open XML WordprocessingML Macro-Enabled Document.

### DOTX {#DOTX}
```
public static int DOTX
```


Saves the document as an Office Open XML WordprocessingML Template (macro-free).

### DOTM {#DOTM}
```
public static int DOTM
```


Saves the document as an Office Open XML WordprocessingML Macro-Enabled Template.

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

### RTF {#RTF}
```
public static int RTF
```


Saves the document in the RTF format. All characters above 7-bits are escaped as hexadecimal or Unicode characters.

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


Saves the document in the Microsoft Word 2003 WordprocessingML format.

### PDF {#PDF}
```
public static int PDF
```


Saves the document as PDF (Adobe Portable Document) format.

### XPS {#XPS}
```
public static int XPS
```


Saves the document in the XPS (XML Paper Specification) format.

### XAML_FIXED {#XAML-FIXED}
```
public static int XAML_FIXED
```


Saves the document in the Extensible Application Markup Language (XAML) format as a fixed document.

### SVG {#SVG}
```
public static int SVG
```


Saves the document in the Svg (Scalable Vector Graphics) format.

### HTML_FIXED {#HTML-FIXED}
```
public static int HTML_FIXED
```


Saves the document in the HTML format using absolutely positioned elements

### OPEN_XPS {#OPEN-XPS}
```
public static int OPEN_XPS
```


Saves the document in the OpenXPS (Ecma-388) format.

### PS {#PS}
```
public static int PS
```


Saves the document in the PS (PostScript) format.

### PCL {#PCL}
```
public static int PCL
```


Saves the document in the PCL (Printer Control Language) format.

### HTML {#HTML}
```
public static int HTML
```


Saves the document in the HTML format.

### MHTML {#MHTML}
```
public static int MHTML
```


Saves the document in the MHTML (Web archive) format.

### EPUB {#EPUB}
```
public static int EPUB
```


Saves the document in the EPUB format.

### AZW_3 {#AZW-3}
```
public static int AZW_3
```


Saves the document in the AZW3 format.

### ODT {#ODT}
```
public static int ODT
```


Saves the document as an ODF Text Document.

### OTT {#OTT}
```
public static int OTT
```


Saves the document as an ODF Text Document Template.

### TEXT {#TEXT}
```
public static int TEXT
```


Saves the document in the plain text format.

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

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


Saves the document in the Markdown format.

### TIFF {#TIFF}
```
public static int TIFF
```


Renders a page or pages of the document and saves them into a single or multipage TIFF file.

### PNG {#PNG}
```
public static int PNG
```


Renders a page of the document and saves it as a PNG file.

### BMP {#BMP}
```
public static int BMP
```


Renders a page of the document and saves it as a BMP file.

### EMF {#EMF}
```
public static int EMF
```


Renders a page of the document and saves it as a vector EMF (Enhanced Meta File) file.

### JPEG {#JPEG}
```
public static int JPEG
```


Renders a page of the document and saves it as a JPEG file.

### GIF {#GIF}
```
public static int GIF
```


Renders a page of the document and saves it as a GIF file.

### length {#length}
```
public static int length
```


### getName(int saveFormat) {#getName-int-}
```
public static String getName(int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
### toString(int saveFormat) {#toString-int-}
```
public static String toString(int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
### fromName(String saveFormatName) {#fromName-java.lang.String-}
```
public static int fromName(String saveFormatName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormatName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
