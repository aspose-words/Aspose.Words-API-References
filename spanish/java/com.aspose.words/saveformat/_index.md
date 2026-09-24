---
title: "SaveFormat"
linktitle: "SaveFormat"
second_title: "Aspose.Words para Java"
description: "Indica el formato en el que se guarda el documento en Java."
type: docs
weight: 595
url: /es/java/com.aspose.words/saveformat/
---

**Inheritance:**
java.lang.Object
```
public class SaveFormat
```

Indica el formato en el que se guarda el documento.

 **Examples:** 

Muestra cómo convertir de formato DOCX a HTML.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 doc.save(getArtifactsDir() + "Document.ConvertToHtml.html", SaveFormat.HTML);
 
```

**M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.SaveFormat)**
## Campos

| Campo | Descripción |
| --- | --- |
| [AZW_3](#AZW-3) | Guarda el documento en formato AZW3. |
| [BMP](#BMP) | Renderiza una página del documento y la guarda como archivo BMP. |
| [DOC](#DOC) | Guarda el documento en el formato Microsoft Word 97 - 2007 Document. |
| [DOCLING](#DOCLING) | Guarda el documento en formato Docling JSON. |
| [DOCM](#DOCM) | Guarda el documento como un Office Open XML WordprocessingML Macro-Enabled Document. |
| [DOCX](#DOCX) | Guarda el documento como un Office Open XML WordprocessingML Document (sin macros). |
| [DOT](#DOT) | Guarda el documento en el formato Microsoft Word 97 - 2007 Template. |
| [DOTM](#DOTM) | Guarda el documento como una Office Open XML WordprocessingML Macro-Enabled Template. |
| [DOTX](#DOTX) | Guarda el documento como una Office Open XML WordprocessingML Template (sin macros). |
| [EMF](#EMF) | Renderiza una página del documento y la guarda como archivo vectorial EMF (Enhanced Meta File). |
| [EPS](#EPS) | Renderiza una página del documento y la guarda como archivo EPS. |
| [EPUB](#EPUB) | Guarda el documento en formato EPUB. |
| [FLAT_OPC](#FLAT-OPC) | Guarda el documento como Office Open XML WordprocessingML almacenado en un archivo XML plano en lugar de un paquete ZIP. |
| [FLAT_OPC_MACRO_ENABLED](#FLAT-OPC-MACRO-ENABLED) | Guarda el documento como Office Open XML WordprocessingML Macro-Enabled Document almacenado en un archivo XML plano en lugar de un paquete ZIP. |
| [FLAT_OPC_TEMPLATE](#FLAT-OPC-TEMPLATE) | Guarda el documento como Office Open XML WordprocessingML Template (macro-free) almacenado en un archivo XML plano en lugar de un paquete ZIP. |
| [FLAT_OPC_TEMPLATE_MACRO_ENABLED](#FLAT-OPC-TEMPLATE-MACRO-ENABLED) | Guarda el documento como Office Open XML WordprocessingML Macro-Enabled Template almacenado en un archivo XML plano en lugar de un paquete ZIP. |
| [GIF](#GIF) | Renderiza una página del documento y la guarda como archivo GIF. |
| [HTML](#HTML) | Guarda el documento en formato HTML. |
| [HTML_FIXED](#HTML-FIXED) | Guarda el documento en formato HTML usando elementos posicionados absolutamente |
| [JPEG](#JPEG) | Renderiza una página del documento y la guarda como archivo JPEG. |
| [MARKDOWN](#MARKDOWN) | Guarda el documento en formato Markdown. |
| [MHTML](#MHTML) | Guarda el documento en formato MHTML (Web archive). |
| [MOBI](#MOBI) | Guarda el documento en formato MOBI. |
| [ODT](#ODT) | Guarda el documento como ODF Text Document. |
| [OPEN_XPS](#OPEN-XPS) | Guarda el documento en formato OpenXPS (Ecma-388). |
| [OTT](#OTT) | Guarda el documento como ODF Text Document Template. |
| [PCL](#PCL) | Guarda el documento en formato PCL (Printer Control Language). |
| [PDF](#PDF) | Guarda el documento como formato PDF (Adobe Portable Document). |
| [PNG](#PNG) | Renderiza una página del documento y la guarda como archivo PNG. |
| [PS](#PS) | Guarda el documento en formato PS (PostScript). |
| [RTF](#RTF) | Guarda el documento en formato RTF. |
| [SVG](#SVG) | Guarda el documento en formato Svg (Scalable Vector Graphics). |
| [TEXT](#TEXT) | Guarda el documento en formato de texto plano. |
| [TIFF](#TIFF) | Renderiza una o varias páginas del documento y las guarda en un archivo TIFF único o multipágina. |
| [UNKNOWN](#UNKNOWN) | Valor predeterminado, valor no válido para el formato de archivo. |
| [WEB_P](#WEB-P) | Renderiza una página del documento y la guarda como archivo WebP. |
| [WORD_ML](#WORD-ML) | Guarda el documento en el formato Microsoft Word 2003 WordprocessingML. |
| [XAML_FIXED](#XAML-FIXED) | Guarda el documento en el formato Extensible Application Markup Language (XAML) como un documento fijo. |
| [XAML_FLOW](#XAML-FLOW) | **Beta.** Guarda el documento en el formato Extensible Application Markup Language (XAML) como un documento fluido. |
| [XAML_FLOW_PACK](#XAML-FLOW-PACK) | **Beta.** Guarda el documento en el formato de paquete Extensible Application Markup Language (XAML) como un documento fluido. |
| [XLSX](#XLSX) | Guarda el documento como un documento Office Open XML SpreadsheetML (sin macros). |
| [XPS](#XPS) | Guarda el documento en el formato XPS (XML Paper Specification). |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String saveFormatName)](#fromName-java.lang.String) |  |
| [getName(int saveFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int saveFormat)](#toString-int) |  |
### AZW_3 {#AZW-3}
```
public static int AZW_3
```


Guarda el documento en formato AZW3.

### BMP {#BMP}
```
public static int BMP
```


Renderiza una página del documento y la guarda como archivo BMP.

### DOC {#DOC}
```
public static int DOC
```


Guarda el documento en el formato Microsoft Word 97 - 2007 Document.

### DOCLING {#DOCLING}
```
public static int DOCLING
```


Guarda el documento en formato Docling JSON.

### DOCM {#DOCM}
```
public static int DOCM
```


Guarda el documento como un Office Open XML WordprocessingML Macro-Enabled Document.

### DOCX {#DOCX}
```
public static int DOCX
```


Guarda el documento como un Office Open XML WordprocessingML Document (sin macros).

### DOT {#DOT}
```
public static int DOT
```


Guarda el documento en el formato Microsoft Word 97 - 2007 Template.

### DOTM {#DOTM}
```
public static int DOTM
```


Guarda el documento como una Office Open XML WordprocessingML Macro-Enabled Template.

### DOTX {#DOTX}
```
public static int DOTX
```


Guarda el documento como una Office Open XML WordprocessingML Template (sin macros).

### EMF {#EMF}
```
public static int EMF
```


Renderiza una página del documento y la guarda como archivo vectorial EMF (Enhanced Meta File).

### EPS {#EPS}
```
public static int EPS
```


Renderiza una página del documento y la guarda como archivo EPS.

### EPUB {#EPUB}
```
public static int EPUB
```


Guarda el documento en formato EPUB.

### FLAT_OPC {#FLAT-OPC}
```
public static int FLAT_OPC
```


Guarda el documento como Office Open XML WordprocessingML almacenado en un archivo XML plano en lugar de un paquete ZIP.

### FLAT_OPC_MACRO_ENABLED {#FLAT-OPC-MACRO-ENABLED}
```
public static int FLAT_OPC_MACRO_ENABLED
```


Guarda el documento como Office Open XML WordprocessingML Macro-Enabled Document almacenado en un archivo XML plano en lugar de un paquete ZIP.

### FLAT_OPC_TEMPLATE {#FLAT-OPC-TEMPLATE}
```
public static int FLAT_OPC_TEMPLATE
```


Guarda el documento como Office Open XML WordprocessingML Template (macro-free) almacenado en un archivo XML plano en lugar de un paquete ZIP.

### FLAT_OPC_TEMPLATE_MACRO_ENABLED {#FLAT-OPC-TEMPLATE-MACRO-ENABLED}
```
public static int FLAT_OPC_TEMPLATE_MACRO_ENABLED
```


Guarda el documento como Office Open XML WordprocessingML Macro-Enabled Template almacenado en un archivo XML plano en lugar de un paquete ZIP.

### GIF {#GIF}
```
public static int GIF
```


Renderiza una página del documento y la guarda como archivo GIF.

### HTML {#HTML}
```
public static int HTML
```


Guarda el documento en formato HTML.

### HTML_FIXED {#HTML-FIXED}
```
public static int HTML_FIXED
```


Guarda el documento en formato HTML usando elementos posicionados absolutamente

### JPEG {#JPEG}
```
public static int JPEG
```


Renderiza una página del documento y la guarda como archivo JPEG.

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


Guarda el documento en formato Markdown.

### MHTML {#MHTML}
```
public static int MHTML
```


Guarda el documento en formato MHTML (Web archive).

### MOBI {#MOBI}
```
public static int MOBI
```


Guarda el documento en formato MOBI.

### ODT {#ODT}
```
public static int ODT
```


Guarda el documento como ODF Text Document.

### OPEN_XPS {#OPEN-XPS}
```
public static int OPEN_XPS
```


Guarda el documento en formato OpenXPS (Ecma-388).

### OTT {#OTT}
```
public static int OTT
```


Guarda el documento como ODF Text Document Template.

### PCL {#PCL}
```
public static int PCL
```


Guarda el documento en formato PCL (Printer Control Language).

### PDF {#PDF}
```
public static int PDF
```


Guarda el documento como formato PDF (Adobe Portable Document).

### PNG {#PNG}
```
public static int PNG
```


Renderiza una página del documento y la guarda como archivo PNG.

### PS {#PS}
```
public static int PS
```


Guarda el documento en formato PS (PostScript).

### RTF {#RTF}
```
public static int RTF
```


Guarda el documento en el formato RTF. Todos los caracteres superiores a 7 bits se escapan como caracteres hexadecimales o Unicode.

### SVG {#SVG}
```
public static int SVG
```


Guarda el documento en formato Svg (Scalable Vector Graphics).

### TEXT {#TEXT}
```
public static int TEXT
```


Guarda el documento en formato de texto plano.

### TIFF {#TIFF}
```
public static int TIFF
```


Renderiza una o varias páginas del documento y las guarda en un archivo TIFF único o multipágina.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Valor predeterminado, valor no válido para el formato de archivo.

### WEB_P {#WEB-P}
```
public static int WEB_P
```


Renderiza una página del documento y la guarda como archivo WebP.

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


Guarda el documento en el formato Microsoft Word 2003 WordprocessingML.

### XAML_FIXED {#XAML-FIXED}
```
public static int XAML_FIXED
```


Guarda el documento en el formato Extensible Application Markup Language (XAML) como un documento fijo.

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


Guarda el documento como un documento Office Open XML SpreadsheetML (sin macros).

### XPS {#XPS}
```
public static int XPS
```


Guarda el documento en el formato XPS (XML Paper Specification).

### length {#length}
```
public static int length
```


### fromName(String saveFormatName) {#fromName-java.lang.String}
```
public static int fromName(String saveFormatName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| saveFormatName | java.lang.String |  |

**Returns:**
int
### getName(int saveFormat) {#getName-int}
```
public static String getName(int saveFormat)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
