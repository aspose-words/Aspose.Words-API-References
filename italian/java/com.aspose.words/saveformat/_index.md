---
title: "SaveFormat"
linktitle: "SaveFormat"
second_title: "Aspose.Words per Java"
description: "Indica il formato in cui il documento viene salvato in Java."
type: docs
weight: 595
url: /it/java/com.aspose.words/saveformat/
---

**Inheritance:**
java.lang.Object
```
public class SaveFormat
```

Indica il formato in cui il documento viene salvato.

 **Examples:** 

Mostra come convertire dal formato DOCX a HTML.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 doc.save(getArtifactsDir() + "Document.ConvertToHtml.html", SaveFormat.HTML);
 
```

**M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.SaveFormat)**
## Campi

| Campo | Descrizione |
| --- | --- |
| [AZW_3](#AZW-3) | Salva il documento nel formato AZW3. |
| [BMP](#BMP) | Renderizza una pagina del documento e la salva come file BMP. |
| [DOC](#DOC) | Salva il documento nel formato Microsoft Word 97 - 2007 Document. |
| [DOCLING](#DOCLING) | Salva il documento nel formato Docling JSON. |
| [DOCM](#DOCM) | Salva il documento come Office Open XML WordprocessingML Macro-Enabled Document. |
| [DOCX](#DOCX) | Salva il documento come Office Open XML WordprocessingML Document (senza macro). |
| [DOT](#DOT) | Salva il documento nel formato Microsoft Word 97 - 2007 Template. |
| [DOTM](#DOTM) | Salva il documento come Office Open XML WordprocessingML Macro-Enabled Template. |
| [DOTX](#DOTX) | Salva il documento come Office Open XML WordprocessingML Template (senza macro). |
| [EMF](#EMF) | Renderizza una pagina del documento e la salva come file vettoriale EMF (Enhanced Meta File). |
| [EPS](#EPS) | Renderizza una pagina del documento e la salva come file EPS. |
| [EPUB](#EPUB) | Salva il documento nel formato EPUB. |
| [FLAT_OPC](#FLAT-OPC) | Salva il documento come Office Open XML WordprocessingML memorizzato in un file XML piatto invece di un pacchetto ZIP. |
| [FLAT_OPC_MACRO_ENABLED](#FLAT-OPC-MACRO-ENABLED) | Salva il documento come Office Open XML WordprocessingML Macro-Enabled Document memorizzato in un file XML piatto invece di un pacchetto ZIP. |
| [FLAT_OPC_TEMPLATE](#FLAT-OPC-TEMPLATE) | Salva il documento come Office Open XML WordprocessingML Template (senza macro) memorizzato in un file XML piatto invece di un pacchetto ZIP. |
| [FLAT_OPC_TEMPLATE_MACRO_ENABLED](#FLAT-OPC-TEMPLATE-MACRO-ENABLED) | Salva il documento come Office Open XML WordprocessingML Macro-Enabled Template memorizzato in un file XML piatto invece di un pacchetto ZIP. |
| [GIF](#GIF) | Renderizza una pagina del documento e la salva come file GIF. |
| [HTML](#HTML) | Salva il documento nel formato HTML. |
| [HTML_FIXED](#HTML-FIXED) | Salva il documento nel formato HTML usando elementi posizionati assolutamente |
| [JPEG](#JPEG) | Renderizza una pagina del documento e la salva come file JPEG. |
| [MARKDOWN](#MARKDOWN) | Salva il documento nel formato Markdown. |
| [MHTML](#MHTML) | Salva il documento nel formato MHTML (archivio web). |
| [MOBI](#MOBI) | Salva il documento nel formato MOBI. |
| [ODT](#ODT) | Salva il documento come ODF Text Document. |
| [OPEN_XPS](#OPEN-XPS) | Salva il documento nel formato OpenXPS (Ecma-388). |
| [OTT](#OTT) | Salva il documento come ODF Text Document Template. |
| [PCL](#PCL) | Salva il documento nel formato PCL (Printer Control Language). |
| [PDF](#PDF) | Salva il documento come formato PDF (Adobe Portable Document). |
| [PNG](#PNG) | Renderizza una pagina del documento e la salva come file PNG. |
| [PS](#PS) | Salva il documento nel formato PS (PostScript). |
| [RTF](#RTF) | Salva il documento nel formato RTF. |
| [SVG](#SVG) | Salva il documento nel formato Svg (Scalable Vector Graphics). |
| [TEXT](#TEXT) | Salva il documento nel formato di testo semplice. |
| [TIFF](#TIFF) | Renderizza una o più pagine del documento e le salva in un file TIFF singolo o multipagina. |
| [UNKNOWN](#UNKNOWN) | Predefinito, valore non valido per il formato file. |
| [WEB_P](#WEB-P) | Renderizza una pagina del documento e la salva come file WebP. |
| [WORD_ML](#WORD-ML) | Salva il documento nel formato Microsoft Word 2003 WordprocessingML. |
| [XAML_FIXED](#XAML-FIXED) | Salva il documento nel formato Extensible Application Markup Language (XAML) come documento fisso. |
| [XAML_FLOW](#XAML-FLOW) | **Beta.** Salva il documento nel formato Extensible Application Markup Language (XAML) come documento a flusso. |
| [XAML_FLOW_PACK](#XAML-FLOW-PACK) | **Beta.** Salva il documento nel formato pacchetto Extensible Application Markup Language (XAML) come documento a flusso. |
| [XLSX](#XLSX) | Salva il documento come documento Office Open XML SpreadsheetML (senza macro). |
| [XPS](#XPS) | Salva il documento nel formato XPS (XML Paper Specification). |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String saveFormatName)](#fromName-java.lang.String) |  |
| [getName(int saveFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int saveFormat)](#toString-int) |  |
### AZW_3 {#AZW-3}
```
public static int AZW_3
```


Salva il documento nel formato AZW3.

### BMP {#BMP}
```
public static int BMP
```


Renderizza una pagina del documento e la salva come file BMP.

### DOC {#DOC}
```
public static int DOC
```


Salva il documento nel formato Microsoft Word 97 - 2007 Document.

### DOCLING {#DOCLING}
```
public static int DOCLING
```


Salva il documento nel formato Docling JSON.

### DOCM {#DOCM}
```
public static int DOCM
```


Salva il documento come Office Open XML WordprocessingML Macro-Enabled Document.

### DOCX {#DOCX}
```
public static int DOCX
```


Salva il documento come Office Open XML WordprocessingML Document (senza macro).

### DOT {#DOT}
```
public static int DOT
```


Salva il documento nel formato Microsoft Word 97 - 2007 Template.

### DOTM {#DOTM}
```
public static int DOTM
```


Salva il documento come Office Open XML WordprocessingML Macro-Enabled Template.

### DOTX {#DOTX}
```
public static int DOTX
```


Salva il documento come Office Open XML WordprocessingML Template (senza macro).

### EMF {#EMF}
```
public static int EMF
```


Renderizza una pagina del documento e la salva come file vettoriale EMF (Enhanced Meta File).

### EPS {#EPS}
```
public static int EPS
```


Renderizza una pagina del documento e la salva come file EPS.

### EPUB {#EPUB}
```
public static int EPUB
```


Salva il documento nel formato EPUB.

### FLAT_OPC {#FLAT-OPC}
```
public static int FLAT_OPC
```


Salva il documento come Office Open XML WordprocessingML memorizzato in un file XML piatto invece di un pacchetto ZIP.

### FLAT_OPC_MACRO_ENABLED {#FLAT-OPC-MACRO-ENABLED}
```
public static int FLAT_OPC_MACRO_ENABLED
```


Salva il documento come Office Open XML WordprocessingML Macro-Enabled Document memorizzato in un file XML piatto invece di un pacchetto ZIP.

### FLAT_OPC_TEMPLATE {#FLAT-OPC-TEMPLATE}
```
public static int FLAT_OPC_TEMPLATE
```


Salva il documento come Office Open XML WordprocessingML Template (senza macro) memorizzato in un file XML piatto invece di un pacchetto ZIP.

### FLAT_OPC_TEMPLATE_MACRO_ENABLED {#FLAT-OPC-TEMPLATE-MACRO-ENABLED}
```
public static int FLAT_OPC_TEMPLATE_MACRO_ENABLED
```


Salva il documento come Office Open XML WordprocessingML Macro-Enabled Template memorizzato in un file XML piatto invece di un pacchetto ZIP.

### GIF {#GIF}
```
public static int GIF
```


Renderizza una pagina del documento e la salva come file GIF.

### HTML {#HTML}
```
public static int HTML
```


Salva il documento nel formato HTML.

### HTML_FIXED {#HTML-FIXED}
```
public static int HTML_FIXED
```


Salva il documento nel formato HTML usando elementi posizionati assolutamente

### JPEG {#JPEG}
```
public static int JPEG
```


Renderizza una pagina del documento e la salva come file JPEG.

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


Salva il documento nel formato Markdown.

### MHTML {#MHTML}
```
public static int MHTML
```


Salva il documento nel formato MHTML (archivio web).

### MOBI {#MOBI}
```
public static int MOBI
```


Salva il documento nel formato MOBI.

### ODT {#ODT}
```
public static int ODT
```


Salva il documento come ODF Text Document.

### OPEN_XPS {#OPEN-XPS}
```
public static int OPEN_XPS
```


Salva il documento nel formato OpenXPS (Ecma-388).

### OTT {#OTT}
```
public static int OTT
```


Salva il documento come ODF Text Document Template.

### PCL {#PCL}
```
public static int PCL
```


Salva il documento nel formato PCL (Printer Control Language).

### PDF {#PDF}
```
public static int PDF
```


Salva il documento come formato PDF (Adobe Portable Document).

### PNG {#PNG}
```
public static int PNG
```


Renderizza una pagina del documento e la salva come file PNG.

### PS {#PS}
```
public static int PS
```


Salva il documento nel formato PS (PostScript).

### RTF {#RTF}
```
public static int RTF
```


Salva il documento nel formato RTF. Tutti i caratteri superiori a 7 bit sono codificati come esadecimali o caratteri Unicode.

### SVG {#SVG}
```
public static int SVG
```


Salva il documento nel formato Svg (Scalable Vector Graphics).

### TEXT {#TEXT}
```
public static int TEXT
```


Salva il documento nel formato di testo semplice.

### TIFF {#TIFF}
```
public static int TIFF
```


Renderizza una o più pagine del documento e le salva in un file TIFF singolo o multipagina.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Predefinito, valore non valido per il formato file.

### WEB_P {#WEB-P}
```
public static int WEB_P
```


Renderizza una pagina del documento e la salva come file WebP.

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


Salva il documento nel formato Microsoft Word 2003 WordprocessingML.

### XAML_FIXED {#XAML-FIXED}
```
public static int XAML_FIXED
```


Salva il documento nel formato Extensible Application Markup Language (XAML) come documento fisso.

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


Salva il documento come documento Office Open XML SpreadsheetML (senza macro).

### XPS {#XPS}
```
public static int XPS
```


Salva il documento nel formato XPS (XML Paper Specification).

### length {#length}
```
public static int length
```


### fromName(String saveFormatName) {#fromName-java.lang.String}
```
public static int fromName(String saveFormatName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| saveFormatName | java.lang.String |  |

**Returns:**
int
### getName(int saveFormat) {#getName-int}
```
public static String getName(int saveFormat)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
