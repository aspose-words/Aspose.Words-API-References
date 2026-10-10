---
title: "SaveFormat"
linktitle: "SaveFormat"
second_title: "Aspose.Words für Java"
description: "Gibt das Format an, in dem das Dokument in Java gespeichert wird."
type: docs
weight: 595
url: /de/java/com.aspose.words/saveformat/
---

**Inheritance:**
java.lang.Object
```
public class SaveFormat
```

Gibt das Format an, in dem das Dokument gespeichert wird.

 **Examples:** 

Zeigt, wie man von DOCX nach HTML konvertiert.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 doc.save(getArtifactsDir() + "Document.ConvertToHtml.html", SaveFormat.HTML);
 
```

**M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.SaveFormat)**
## Felder

| Feld | Beschreibung |
| --- | --- |
| [AZW_3](#AZW-3) | Speichert das Dokument im AZW3-Format. |
| [BMP](#BMP) | Rendert eine Seite des Dokuments und speichert sie als BMP-Datei. |
| [DOC](#DOC) | Speichert das Dokument im Microsoft Word 97‑2007-Dokumentformat. |
| [DOCLING](#DOCLING) | Speichert das Dokument im Docling‑JSON-Format. |
| [DOCM](#DOCM) | Speichert das Dokument als Office Open XML WordprocessingML Makro‑aktiviertes Dokument. |
| [DOCX](#DOCX) | Speichert das Dokument als Office Open XML WordprocessingML Dokument (makrofrei). |
| [DOT](#DOT) | Speichert das Dokument im Microsoft Word 97‑2007-Vorlagenformat. |
| [DOTM](#DOTM) | Speichert das Dokument als Office Open XML WordprocessingML Makro‑aktivierte Vorlage. |
| [DOTX](#DOTX) | Speichert das Dokument als Office Open XML WordprocessingML Vorlage (makrofrei). |
| [EMF](#EMF) | Rendert eine Seite des Dokuments und speichert sie als Vektor‑EMF (Enhanced Meta File)-Datei. |
| [EPS](#EPS) | Rendert eine Seite des Dokuments und speichert sie als EPS-Datei. |
| [EPUB](#EPUB) | Speichert das Dokument im EPUB-Format. |
| [FLAT_OPC](#FLAT-OPC) | Speichert das Dokument als Office Open XML WordprocessingML, das in einer flachen XML-Datei anstelle eines ZIP-Pakets gespeichert wird. |
| [FLAT_OPC_MACRO_ENABLED](#FLAT-OPC-MACRO-ENABLED) | Speichert das Dokument als Office Open XML WordprocessingML-Makroaktiviertes Dokument, das in einer flachen XML-Datei anstelle eines ZIP-Pakets gespeichert wird. |
| [FLAT_OPC_TEMPLATE](#FLAT-OPC-TEMPLATE) | Speichert das Dokument als Office Open XML WordprocessingML-Vorlage (makrofrei), die in einer flachen XML-Datei anstelle eines ZIP-Pakets gespeichert wird. |
| [FLAT_OPC_TEMPLATE_MACRO_ENABLED](#FLAT-OPC-TEMPLATE-MACRO-ENABLED) | Speichert das Dokument als Office Open XML WordprocessingML-Makroaktivierte Vorlage, die in einer flachen XML-Datei anstelle eines ZIP-Pakets gespeichert wird. |
| [GIF](#GIF) | Rendert eine Seite des Dokuments und speichert sie als GIF-Datei. |
| [HTML](#HTML) | Speichert das Dokument im HTML-Format. |
| [HTML_FIXED](#HTML-FIXED) | Speichert das Dokument im HTML-Format unter Verwendung absolut positionierter Elemente |
| [JPEG](#JPEG) | Rendert eine Seite des Dokuments und speichert sie als JPEG-Datei. |
| [MARKDOWN](#MARKDOWN) | Speichert das Dokument im Markdown-Format. |
| [MHTML](#MHTML) | Speichert das Dokument im MHTML-Format (Web-Archiv). |
| [MOBI](#MOBI) | Speichert das Dokument im MOBI-Format. |
| [ODT](#ODT) | Speichert das Dokument als ODF-Textdokument. |
| [OPEN_XPS](#OPEN-XPS) | Speichert das Dokument im OpenXPS-Format (Ecma-388). |
| [OTT](#OTT) | Speichert das Dokument als ODF-Textdokumentvorlage. |
| [PCL](#PCL) | Speichert das Dokument im PCL-Format (Printer Control Language). |
| [PDF](#PDF) | Speichert das Dokument im PDF-Format (Adobe Portable Document). |
| [PNG](#PNG) | Rendert eine Seite des Dokuments und speichert sie als PNG-Datei. |
| [PS](#PS) | Speichert das Dokument im PS-Format (PostScript). |
| [RTF](#RTF) | Speichert das Dokument im RTF-Format. |
| [SVG](#SVG) | Speichert das Dokument im SVG-Format (Scalable Vector Graphics). |
| [TEXT](#TEXT) | Speichert das Dokument im Klartextformat. |
| [TIFF](#TIFF) | Rendert eine oder mehrere Seiten des Dokuments und speichert sie in einer einzelnen oder mehrseitigen TIFF-Datei. |
| [UNKNOWN](#UNKNOWN) | Standard, ungültiger Wert für das Dateiformat. |
| [WEB_P](#WEB-P) | Rendert eine Seite des Dokuments und speichert sie als WebP-Datei. |
| [WORD_ML](#WORD-ML) | Speichert das Dokument im Microsoft Word 2003 WordprocessingML-Format. |
| [XAML_FIXED](#XAML-FIXED) | Speichert das Dokument im Extensible Application Markup Language (XAML)-Format als festes Dokument. |
| [XAML_FLOW](#XAML-FLOW) | **Beta.** Speichert das Dokument im Extensible Application Markup Language (XAML)-Format als Flussdokument. |
| [XAML_FLOW_PACK](#XAML-FLOW-PACK) | **Beta.** Speichert das Dokument im Extensible Application Markup Language (XAML)-Paketformat als Flussdokument. |
| [XLSX](#XLSX) | Speichert das Dokument als Office Open XML SpreadsheetML-Dokument (makrofrei). |
| [XPS](#XPS) | Speichert das Dokument im XPS (XML Paper Specification)-Format. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String saveFormatName)](#fromName-java.lang.String) |  |
| [getName(int saveFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int saveFormat)](#toString-int) |  |
### AZW_3 {#AZW-3}
```
public static int AZW_3
```


Speichert das Dokument im AZW3-Format.

### BMP {#BMP}
```
public static int BMP
```


Rendert eine Seite des Dokuments und speichert sie als BMP-Datei.

### DOC {#DOC}
```
public static int DOC
```


Speichert das Dokument im Microsoft Word 97‑2007-Dokumentformat.

### DOCLING {#DOCLING}
```
public static int DOCLING
```


Speichert das Dokument im Docling‑JSON-Format.

### DOCM {#DOCM}
```
public static int DOCM
```


Speichert das Dokument als Office Open XML WordprocessingML Makro‑aktiviertes Dokument.

### DOCX {#DOCX}
```
public static int DOCX
```


Speichert das Dokument als Office Open XML WordprocessingML Dokument (makrofrei).

### DOT {#DOT}
```
public static int DOT
```


Speichert das Dokument im Microsoft Word 97‑2007-Vorlagenformat.

### DOTM {#DOTM}
```
public static int DOTM
```


Speichert das Dokument als Office Open XML WordprocessingML Makro‑aktivierte Vorlage.

### DOTX {#DOTX}
```
public static int DOTX
```


Speichert das Dokument als Office Open XML WordprocessingML Vorlage (makrofrei).

### EMF {#EMF}
```
public static int EMF
```


Rendert eine Seite des Dokuments und speichert sie als Vektor‑EMF (Enhanced Meta File)-Datei.

### EPS {#EPS}
```
public static int EPS
```


Rendert eine Seite des Dokuments und speichert sie als EPS-Datei.

### EPUB {#EPUB}
```
public static int EPUB
```


Speichert das Dokument im EPUB-Format.

### FLAT_OPC {#FLAT-OPC}
```
public static int FLAT_OPC
```


Speichert das Dokument als Office Open XML WordprocessingML, das in einer flachen XML-Datei anstelle eines ZIP-Pakets gespeichert wird.

### FLAT_OPC_MACRO_ENABLED {#FLAT-OPC-MACRO-ENABLED}
```
public static int FLAT_OPC_MACRO_ENABLED
```


Speichert das Dokument als Office Open XML WordprocessingML-Makroaktiviertes Dokument, das in einer flachen XML-Datei anstelle eines ZIP-Pakets gespeichert wird.

### FLAT_OPC_TEMPLATE {#FLAT-OPC-TEMPLATE}
```
public static int FLAT_OPC_TEMPLATE
```


Speichert das Dokument als Office Open XML WordprocessingML-Vorlage (makrofrei), die in einer flachen XML-Datei anstelle eines ZIP-Pakets gespeichert wird.

### FLAT_OPC_TEMPLATE_MACRO_ENABLED {#FLAT-OPC-TEMPLATE-MACRO-ENABLED}
```
public static int FLAT_OPC_TEMPLATE_MACRO_ENABLED
```


Speichert das Dokument als Office Open XML WordprocessingML-Makroaktivierte Vorlage, die in einer flachen XML-Datei anstelle eines ZIP-Pakets gespeichert wird.

### GIF {#GIF}
```
public static int GIF
```


Rendert eine Seite des Dokuments und speichert sie als GIF-Datei.

### HTML {#HTML}
```
public static int HTML
```


Speichert das Dokument im HTML-Format.

### HTML_FIXED {#HTML-FIXED}
```
public static int HTML_FIXED
```


Speichert das Dokument im HTML-Format unter Verwendung absolut positionierter Elemente

### JPEG {#JPEG}
```
public static int JPEG
```


Rendert eine Seite des Dokuments und speichert sie als JPEG-Datei.

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


Speichert das Dokument im Markdown-Format.

### MHTML {#MHTML}
```
public static int MHTML
```


Speichert das Dokument im MHTML-Format (Web-Archiv).

### MOBI {#MOBI}
```
public static int MOBI
```


Speichert das Dokument im MOBI-Format.

### ODT {#ODT}
```
public static int ODT
```


Speichert das Dokument als ODF-Textdokument.

### OPEN_XPS {#OPEN-XPS}
```
public static int OPEN_XPS
```


Speichert das Dokument im OpenXPS-Format (Ecma-388).

### OTT {#OTT}
```
public static int OTT
```


Speichert das Dokument als ODF-Textdokumentvorlage.

### PCL {#PCL}
```
public static int PCL
```


Speichert das Dokument im PCL-Format (Printer Control Language).

### PDF {#PDF}
```
public static int PDF
```


Speichert das Dokument im PDF-Format (Adobe Portable Document).

### PNG {#PNG}
```
public static int PNG
```


Rendert eine Seite des Dokuments und speichert sie als PNG-Datei.

### PS {#PS}
```
public static int PS
```


Speichert das Dokument im PS-Format (PostScript).

### RTF {#RTF}
```
public static int RTF
```


Speichert das Dokument im RTF-Format. Alle Zeichen über 7 Bit werden als hexadezimale oder Unicode-Zeichen maskiert.

### SVG {#SVG}
```
public static int SVG
```


Speichert das Dokument im SVG-Format (Scalable Vector Graphics).

### TEXT {#TEXT}
```
public static int TEXT
```


Speichert das Dokument im Klartextformat.

### TIFF {#TIFF}
```
public static int TIFF
```


Rendert eine oder mehrere Seiten des Dokuments und speichert sie in einer einzelnen oder mehrseitigen TIFF-Datei.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Standard, ungültiger Wert für das Dateiformat.

### WEB_P {#WEB-P}
```
public static int WEB_P
```


Rendert eine Seite des Dokuments und speichert sie als WebP-Datei.

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


Speichert das Dokument im Microsoft Word 2003 WordprocessingML-Format.

### XAML_FIXED {#XAML-FIXED}
```
public static int XAML_FIXED
```


Speichert das Dokument im Extensible Application Markup Language (XAML)-Format als festes Dokument.

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


Speichert das Dokument als Office Open XML SpreadsheetML-Dokument (makrofrei).

### XPS {#XPS}
```
public static int XPS
```


Speichert das Dokument im XPS (XML Paper Specification)-Format.

### length {#length}
```
public static int length
```


### fromName(String saveFormatName) {#fromName-java.lang.String}
```
public static int fromName(String saveFormatName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| saveFormatName | java.lang.String |  |

**Returns:**
int
### getName(int saveFormat) {#getName-int}
```
public static String getName(int saveFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
