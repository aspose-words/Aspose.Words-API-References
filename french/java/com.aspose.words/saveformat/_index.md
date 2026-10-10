---
title: "SaveFormat"
linktitle: "SaveFormat"
second_title: "Aspose.Words pour Java"
description: "Indique le format dans lequel le document est enregistré en Java."
type: docs
weight: 595
url: /fr/java/com.aspose.words/saveformat/
---

**Inheritance:**
java.lang.Object
```
public class SaveFormat
```

Indique le format dans lequel le document est enregistré.

 **Examples:** 

Montre comment convertir du format DOCX au format HTML.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 doc.save(getArtifactsDir() + "Document.ConvertToHtml.html", SaveFormat.HTML);
 
```

**M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.SaveFormat)**
## Champs

| Champ | Description |
| --- | --- |
| [AZW_3](#AZW-3) | Enregistre le document au format AZW3. |
| [BMP](#BMP) | Rend une page du document et l'enregistre en tant que fichier BMP. |
| [DOC](#DOC) | Enregistre le document au format Microsoft Word 97 - 2007 Document. |
| [DOCLING](#DOCLING) | Enregistre le document au format Docling JSON. |
| [DOCM](#DOCM) | Enregistre le document en tant que Office Open XML WordprocessingML Macro-Enabled Document. |
| [DOCX](#DOCX) | Enregistre le document en tant que Office Open XML WordprocessingML Document (sans macro). |
| [DOT](#DOT) | Enregistre le document au format Microsoft Word 97 - 2007 Template. |
| [DOTM](#DOTM) | Enregistre le document en tant que Office Open XML WordprocessingML Macro-Enabled Template. |
| [DOTX](#DOTX) | Enregistre le document en tant que Office Open XML WordprocessingML Template (sans macro). |
| [EMF](#EMF) | Rend une page du document et l'enregistre en tant que fichier vectoriel EMF (Enhanced Meta File). |
| [EPS](#EPS) | Rend une page du document et l'enregistre en tant que fichier EPS. |
| [EPUB](#EPUB) | Enregistre le document au format EPUB. |
| [FLAT_OPC](#FLAT-OPC) | Enregistre le document en tant que Office Open XML WordprocessingML stocké dans un fichier XML plat au lieu d'un paquet ZIP. |
| [FLAT_OPC_MACRO_ENABLED](#FLAT-OPC-MACRO-ENABLED) | Enregistre le document en tant que Office Open XML WordprocessingML Macro-Enabled Document stocké dans un fichier XML plat au lieu d'un paquet ZIP. |
| [FLAT_OPC_TEMPLATE](#FLAT-OPC-TEMPLATE) | Enregistre le document en tant que Office Open XML WordprocessingML Template (macro-free) stocké dans un fichier XML plat au lieu d'un paquet ZIP. |
| [FLAT_OPC_TEMPLATE_MACRO_ENABLED](#FLAT-OPC-TEMPLATE-MACRO-ENABLED) | Enregistre le document en tant que Office Open XML WordprocessingML Macro-Enabled Template stocké dans un fichier XML plat au lieu d'un paquet ZIP. |
| [GIF](#GIF) | Rend une page du document et l'enregistre au format GIF. |
| [HTML](#HTML) | Enregistre le document au format HTML. |
| [HTML_FIXED](#HTML-FIXED) | Enregistre le document au format HTML en utilisant des éléments positionnés absolument |
| [JPEG](#JPEG) | Rend une page du document et l'enregistre au format JPEG. |
| [MARKDOWN](#MARKDOWN) | Enregistre le document au format Markdown. |
| [MHTML](#MHTML) | Enregistre le document au format MHTML (Web archive). |
| [MOBI](#MOBI) | Enregistre le document au format MOBI. |
| [ODT](#ODT) | Enregistre le document en tant que ODF Text Document. |
| [OPEN_XPS](#OPEN-XPS) | Enregistre le document au format OpenXPS (Ecma-388). |
| [OTT](#OTT) | Enregistre le document en tant que ODF Text Document Template. |
| [PCL](#PCL) | Enregistre le document au format PCL (Printer Control Language). |
| [PDF](#PDF) | Enregistre le document au format PDF (Adobe Portable Document). |
| [PNG](#PNG) | Rend une page du document et l'enregistre au format PNG. |
| [PS](#PS) | Enregistre le document au format PS (PostScript). |
| [RTF](#RTF) | Enregistre le document au format RTF. |
| [SVG](#SVG) | Enregistre le document au format Svg (Scalable Vector Graphics). |
| [TEXT](#TEXT) | Enregistre le document au format texte brut. |
| [TIFF](#TIFF) | Rend une ou plusieurs pages du document et les enregistre dans un fichier TIFF simple ou multipage. |
| [UNKNOWN](#UNKNOWN) | Valeur par défaut, valeur non valide pour le format de fichier. |
| [WEB_P](#WEB-P) | Rend une page du document et l'enregistre au format WebP. |
| [WORD_ML](#WORD-ML) | Enregistre le document au format Microsoft Word 2003 WordprocessingML. |
| [XAML_FIXED](#XAML-FIXED) | Enregistre le document au format Extensible Application Markup Language (XAML) en tant que document fixe. |
| [XAML_FLOW](#XAML-FLOW) | **Beta.** Enregistre le document au format Extensible Application Markup Language (XAML) en tant que document flux. |
| [XAML_FLOW_PACK](#XAML-FLOW-PACK) | **Beta.** Enregistre le document au format Extensible Application Markup Language (XAML) package en tant que document flux. |
| [XLSX](#XLSX) | Enregistre le document en tant que document Office Open XML SpreadsheetML (sans macro). |
| [XPS](#XPS) | Enregistre le document au format XPS (XML Paper Specification). |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String saveFormatName)](#fromName-java.lang.String) |  |
| [getName(int saveFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int saveFormat)](#toString-int) |  |
### AZW_3 {#AZW-3}
```
public static int AZW_3
```


Enregistre le document au format AZW3.

### BMP {#BMP}
```
public static int BMP
```


Rend une page du document et l'enregistre en tant que fichier BMP.

### DOC {#DOC}
```
public static int DOC
```


Enregistre le document au format Microsoft Word 97 - 2007 Document.

### DOCLING {#DOCLING}
```
public static int DOCLING
```


Enregistre le document au format Docling JSON.

### DOCM {#DOCM}
```
public static int DOCM
```


Enregistre le document en tant que Office Open XML WordprocessingML Macro-Enabled Document.

### DOCX {#DOCX}
```
public static int DOCX
```


Enregistre le document en tant que Office Open XML WordprocessingML Document (sans macro).

### DOT {#DOT}
```
public static int DOT
```


Enregistre le document au format Microsoft Word 97 - 2007 Template.

### DOTM {#DOTM}
```
public static int DOTM
```


Enregistre le document en tant que Office Open XML WordprocessingML Macro-Enabled Template.

### DOTX {#DOTX}
```
public static int DOTX
```


Enregistre le document en tant que Office Open XML WordprocessingML Template (sans macro).

### EMF {#EMF}
```
public static int EMF
```


Rend une page du document et l'enregistre en tant que fichier vectoriel EMF (Enhanced Meta File).

### EPS {#EPS}
```
public static int EPS
```


Rend une page du document et l'enregistre en tant que fichier EPS.

### EPUB {#EPUB}
```
public static int EPUB
```


Enregistre le document au format EPUB.

### FLAT_OPC {#FLAT-OPC}
```
public static int FLAT_OPC
```


Enregistre le document en tant que Office Open XML WordprocessingML stocké dans un fichier XML plat au lieu d'un paquet ZIP.

### FLAT_OPC_MACRO_ENABLED {#FLAT-OPC-MACRO-ENABLED}
```
public static int FLAT_OPC_MACRO_ENABLED
```


Enregistre le document en tant que Office Open XML WordprocessingML Macro-Enabled Document stocké dans un fichier XML plat au lieu d'un paquet ZIP.

### FLAT_OPC_TEMPLATE {#FLAT-OPC-TEMPLATE}
```
public static int FLAT_OPC_TEMPLATE
```


Enregistre le document en tant que Office Open XML WordprocessingML Template (macro-free) stocké dans un fichier XML plat au lieu d'un paquet ZIP.

### FLAT_OPC_TEMPLATE_MACRO_ENABLED {#FLAT-OPC-TEMPLATE-MACRO-ENABLED}
```
public static int FLAT_OPC_TEMPLATE_MACRO_ENABLED
```


Enregistre le document en tant que Office Open XML WordprocessingML Macro-Enabled Template stocké dans un fichier XML plat au lieu d'un paquet ZIP.

### GIF {#GIF}
```
public static int GIF
```


Rend une page du document et l'enregistre au format GIF.

### HTML {#HTML}
```
public static int HTML
```


Enregistre le document au format HTML.

### HTML_FIXED {#HTML-FIXED}
```
public static int HTML_FIXED
```


Enregistre le document au format HTML en utilisant des éléments positionnés absolument

### JPEG {#JPEG}
```
public static int JPEG
```


Rend une page du document et l'enregistre au format JPEG.

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


Enregistre le document au format Markdown.

### MHTML {#MHTML}
```
public static int MHTML
```


Enregistre le document au format MHTML (Web archive).

### MOBI {#MOBI}
```
public static int MOBI
```


Enregistre le document au format MOBI.

### ODT {#ODT}
```
public static int ODT
```


Enregistre le document en tant que ODF Text Document.

### OPEN_XPS {#OPEN-XPS}
```
public static int OPEN_XPS
```


Enregistre le document au format OpenXPS (Ecma-388).

### OTT {#OTT}
```
public static int OTT
```


Enregistre le document en tant que ODF Text Document Template.

### PCL {#PCL}
```
public static int PCL
```


Enregistre le document au format PCL (Printer Control Language).

### PDF {#PDF}
```
public static int PDF
```


Enregistre le document au format PDF (Adobe Portable Document).

### PNG {#PNG}
```
public static int PNG
```


Rend une page du document et l'enregistre au format PNG.

### PS {#PS}
```
public static int PS
```


Enregistre le document au format PS (PostScript).

### RTF {#RTF}
```
public static int RTF
```


Enregistre le document au format RTF. Tous les caractères supérieurs à 7 bits sont échappés en hexadécimal ou en caractères Unicode.

### SVG {#SVG}
```
public static int SVG
```


Enregistre le document au format Svg (Scalable Vector Graphics).

### TEXT {#TEXT}
```
public static int TEXT
```


Enregistre le document au format texte brut.

### TIFF {#TIFF}
```
public static int TIFF
```


Rend une ou plusieurs pages du document et les enregistre dans un fichier TIFF simple ou multipage.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Valeur par défaut, valeur non valide pour le format de fichier.

### WEB_P {#WEB-P}
```
public static int WEB_P
```


Rend une page du document et l'enregistre au format WebP.

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


Enregistre le document au format Microsoft Word 2003 WordprocessingML.

### XAML_FIXED {#XAML-FIXED}
```
public static int XAML_FIXED
```


Enregistre le document au format Extensible Application Markup Language (XAML) en tant que document fixe.

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


Enregistre le document en tant que document Office Open XML SpreadsheetML (sans macro).

### XPS {#XPS}
```
public static int XPS
```


Enregistre le document au format XPS (XML Paper Specification).

### length {#length}
```
public static int length
```


### fromName(String saveFormatName) {#fromName-java.lang.String}
```
public static int fromName(String saveFormatName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| saveFormatName | java.lang.String |  |

**Returns:**
int
### getName(int saveFormat) {#getName-int}
```
public static String getName(int saveFormat)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
