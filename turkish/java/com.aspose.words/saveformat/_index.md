---
title: "SaveFormat"
linktitle: "SaveFormat"
second_title: "Aspose.Words Java için"
description: "Java'da belgenin kaydedildiği formatı gösterir."
type: docs
weight: 595
url: /tr/java/com.aspose.words/saveformat/
---

**Inheritance:**
java.lang.Object
```
public class SaveFormat
```

Belgenin kaydedildiği formatı gösterir.

 **Examples:** 

DOCX'ten HTML formatına nasıl dönüştürüleceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 doc.save(getArtifactsDir() + "Document.ConvertToHtml.html", SaveFormat.HTML);
 
```

**M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.SaveFormat)**
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [AZW_3](#AZW-3) | Belgeyi AZW3 formatında kaydeder. |
| [BMP](#BMP) | Belgenin bir sayfasını işler ve BMP dosyası olarak kaydeder. |
| [DOC](#DOC) | Belgeyi Microsoft Word 97 - 2007 Belge formatında kaydeder. |
| [DOCLING](#DOCLING) | Belgeyi Docling JSON formatında kaydeder. |
| [DOCM](#DOCM) | Belgeyi Office Open XML WordprocessingML Makro Etkin Belge olarak kaydeder. |
| [DOCX](#DOCX) | Belgeyi Office Open XML WordprocessingML Belge (makrosuz) olarak kaydeder. |
| [DOT](#DOT) | Belgeyi Microsoft Word 97 - 2007 Şablon formatında kaydeder. |
| [DOTM](#DOTM) | Belgeyi Office Open XML WordprocessingML Makro Etkin Şablon olarak kaydeder. |
| [DOTX](#DOTX) | Belgeyi Office Open XML WordprocessingML Şablon (makrosuz) olarak kaydeder. |
| [EMF](#EMF) | Belgenin bir sayfasını işler ve vektör EMF (Gelişmiş Meta Dosya) dosyası olarak kaydeder. |
| [EPS](#EPS) | Belgenin bir sayfasını işler ve EPS dosyası olarak kaydeder. |
| [EPUB](#EPUB) | Belgeyi EPUB formatında kaydeder. |
| [FLAT_OPC](#FLAT-OPC) | Belgeyi, ZIP paketi yerine düz bir XML dosyasında depolanan Office Open XML WordprocessingML olarak kaydeder. |
| [FLAT_OPC_MACRO_ENABLED](#FLAT-OPC-MACRO-ENABLED) | Belgeyi, ZIP paketi yerine düz bir XML dosyasında depolanan Makro Etkin Office Open XML WordprocessingML Belgesi olarak kaydeder. |
| [FLAT_OPC_TEMPLATE](#FLAT-OPC-TEMPLATE) | Belgeyi, ZIP paketi yerine düz bir XML dosyasında depolanan (makrosuz) Office Open XML WordprocessingML Şablonu olarak kaydeder. |
| [FLAT_OPC_TEMPLATE_MACRO_ENABLED](#FLAT-OPC-TEMPLATE-MACRO-ENABLED) | Belgeyi, ZIP paketi yerine düz bir XML dosyasında depolanan Makro Etkin Office Open XML WordprocessingML Şablonu olarak kaydeder. |
| [GIF](#GIF) | Belgenin bir sayfasını işler ve GIF dosyası olarak kaydeder. |
| [HTML](#HTML) | Belgeyi HTML formatında kaydeder. |
| [HTML_FIXED](#HTML-FIXED) | Belgeyi mutlak konumlandırılmış öğeler kullanarak HTML formatında kaydeder. |
| [JPEG](#JPEG) | Belgenin bir sayfasını işler ve JPEG dosyası olarak kaydeder. |
| [MARKDOWN](#MARKDOWN) | Belgeyi Markdown formatında kaydeder. |
| [MHTML](#MHTML) | Belgeyi MHTML (Web arşivi) formatında kaydeder. |
| [MOBI](#MOBI) | Belgeyi MOBI formatında kaydeder. |
| [ODT](#ODT) | Belgeyi ODF Metin Belgesi olarak kaydeder. |
| [OPEN_XPS](#OPEN-XPS) | Belgeyi OpenXPS (Ecma-388) formatında kaydeder. |
| [OTT](#OTT) | Belgeyi ODF Metin Belgesi Şablonu olarak kaydeder. |
| [PCL](#PCL) | Belgeyi PCL (Yazıcı Kontrol Dili) formatında kaydeder. |
| [PDF](#PDF) | Belgeyi PDF (Adobe Taşınabilir Belge) formatında kaydeder. |
| [PNG](#PNG) | Belgenin bir sayfasını işler ve PNG dosyası olarak kaydeder. |
| [PS](#PS) | Belgeyi PS (PostScript) formatında kaydeder. |
| [RTF](#RTF) | Belgeyi RTF formatında kaydeder. |
| [SVG](#SVG) | Belgeyi Svg (Ölçeklenebilir Vektör Grafikleri) formatında kaydeder. |
| [TEXT](#TEXT) | Belgeyi düz metin formatında kaydeder. |
| [TIFF](#TIFF) | Belgenin bir veya birden fazla sayfasını işler ve tekli ya da çok sayfalı TIFF dosyası olarak kaydeder. |
| [UNKNOWN](#UNKNOWN) | Varsayılan, dosya formatı için geçersiz değer. |
| [WEB_P](#WEB-P) | Belgenin bir sayfasını işler ve WebP dosyası olarak kaydeder. |
| [WORD_ML](#WORD-ML) | Belgeyi Microsoft Word 2003 WordprocessingML biçiminde kaydeder. |
| [XAML_FIXED](#XAML-FIXED) | Belgeyi Extensible Application Markup Language (XAML) biçiminde sabit bir belge olarak kaydeder. |
| [XAML_FLOW](#XAML-FLOW) | **Beta.** Belgeyi Extensible Application Markup Language (XAML) biçiminde akış belgesi olarak kaydeder. |
| [XAML_FLOW_PACK](#XAML-FLOW-PACK) | **Beta.** Belgeyi Extensible Application Markup Language (XAML) paket biçiminde akış belgesi olarak kaydeder. |
| [XLSX](#XLSX) | Belgeyi Office Open XML SpreadsheetML Belgesi (makro içermeyen) olarak kaydeder. |
| [XPS](#XPS) | Belgeyi XPS (XML Paper Specification) biçiminde kaydeder. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String saveFormatName)](#fromName-java.lang.String) |  |
| [getName(int saveFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int saveFormat)](#toString-int) |  |
### AZW_3 {#AZW-3}
```
public static int AZW_3
```


Belgeyi AZW3 formatında kaydeder.

### BMP {#BMP}
```
public static int BMP
```


Belgenin bir sayfasını işler ve BMP dosyası olarak kaydeder.

### DOC {#DOC}
```
public static int DOC
```


Belgeyi Microsoft Word 97 - 2007 Belge formatında kaydeder.

### DOCLING {#DOCLING}
```
public static int DOCLING
```


Belgeyi Docling JSON formatında kaydeder.

### DOCM {#DOCM}
```
public static int DOCM
```


Belgeyi Office Open XML WordprocessingML Makro Etkin Belge olarak kaydeder.

### DOCX {#DOCX}
```
public static int DOCX
```


Belgeyi Office Open XML WordprocessingML Belge (makrosuz) olarak kaydeder.

### DOT {#DOT}
```
public static int DOT
```


Belgeyi Microsoft Word 97 - 2007 Şablon formatında kaydeder.

### DOTM {#DOTM}
```
public static int DOTM
```


Belgeyi Office Open XML WordprocessingML Makro Etkin Şablon olarak kaydeder.

### DOTX {#DOTX}
```
public static int DOTX
```


Belgeyi Office Open XML WordprocessingML Şablon (makrosuz) olarak kaydeder.

### EMF {#EMF}
```
public static int EMF
```


Belgenin bir sayfasını işler ve vektör EMF (Gelişmiş Meta Dosya) dosyası olarak kaydeder.

### EPS {#EPS}
```
public static int EPS
```


Belgenin bir sayfasını işler ve EPS dosyası olarak kaydeder.

### EPUB {#EPUB}
```
public static int EPUB
```


Belgeyi EPUB formatında kaydeder.

### FLAT_OPC {#FLAT-OPC}
```
public static int FLAT_OPC
```


Belgeyi, ZIP paketi yerine düz bir XML dosyasında depolanan Office Open XML WordprocessingML olarak kaydeder.

### FLAT_OPC_MACRO_ENABLED {#FLAT-OPC-MACRO-ENABLED}
```
public static int FLAT_OPC_MACRO_ENABLED
```


Belgeyi, ZIP paketi yerine düz bir XML dosyasında depolanan Makro Etkin Office Open XML WordprocessingML Belgesi olarak kaydeder.

### FLAT_OPC_TEMPLATE {#FLAT-OPC-TEMPLATE}
```
public static int FLAT_OPC_TEMPLATE
```


Belgeyi, ZIP paketi yerine düz bir XML dosyasında depolanan (makrosuz) Office Open XML WordprocessingML Şablonu olarak kaydeder.

### FLAT_OPC_TEMPLATE_MACRO_ENABLED {#FLAT-OPC-TEMPLATE-MACRO-ENABLED}
```
public static int FLAT_OPC_TEMPLATE_MACRO_ENABLED
```


Belgeyi, ZIP paketi yerine düz bir XML dosyasında depolanan Makro Etkin Office Open XML WordprocessingML Şablonu olarak kaydeder.

### GIF {#GIF}
```
public static int GIF
```


Belgenin bir sayfasını işler ve GIF dosyası olarak kaydeder.

### HTML {#HTML}
```
public static int HTML
```


Belgeyi HTML formatında kaydeder.

### HTML_FIXED {#HTML-FIXED}
```
public static int HTML_FIXED
```


Belgeyi mutlak konumlandırılmış öğeler kullanarak HTML formatında kaydeder.

### JPEG {#JPEG}
```
public static int JPEG
```


Belgenin bir sayfasını işler ve JPEG dosyası olarak kaydeder.

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


Belgeyi Markdown formatında kaydeder.

### MHTML {#MHTML}
```
public static int MHTML
```


Belgeyi MHTML (Web arşivi) formatında kaydeder.

### MOBI {#MOBI}
```
public static int MOBI
```


Belgeyi MOBI formatında kaydeder.

### ODT {#ODT}
```
public static int ODT
```


Belgeyi ODF Metin Belgesi olarak kaydeder.

### OPEN_XPS {#OPEN-XPS}
```
public static int OPEN_XPS
```


Belgeyi OpenXPS (Ecma-388) formatında kaydeder.

### OTT {#OTT}
```
public static int OTT
```


Belgeyi ODF Metin Belgesi Şablonu olarak kaydeder.

### PCL {#PCL}
```
public static int PCL
```


Belgeyi PCL (Yazıcı Kontrol Dili) formatında kaydeder.

### PDF {#PDF}
```
public static int PDF
```


Belgeyi PDF (Adobe Taşınabilir Belge) formatında kaydeder.

### PNG {#PNG}
```
public static int PNG
```


Belgenin bir sayfasını işler ve PNG dosyası olarak kaydeder.

### PS {#PS}
```
public static int PS
```


Belgeyi PS (PostScript) formatında kaydeder.

### RTF {#RTF}
```
public static int RTF
```


Belgeyi RTF biçiminde kaydeder. 7 bitten büyük tüm karakterler onaltılık ya da Unicode karakterler olarak kaçış yapılır.

### SVG {#SVG}
```
public static int SVG
```


Belgeyi Svg (Ölçeklenebilir Vektör Grafikleri) formatında kaydeder.

### TEXT {#TEXT}
```
public static int TEXT
```


Belgeyi düz metin formatında kaydeder.

### TIFF {#TIFF}
```
public static int TIFF
```


Belgenin bir veya birden fazla sayfasını işler ve tekli ya da çok sayfalı TIFF dosyası olarak kaydeder.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Varsayılan, dosya formatı için geçersiz değer.

### WEB_P {#WEB-P}
```
public static int WEB_P
```


Belgenin bir sayfasını işler ve WebP dosyası olarak kaydeder.

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


Belgeyi Microsoft Word 2003 WordprocessingML biçiminde kaydeder.

### XAML_FIXED {#XAML-FIXED}
```
public static int XAML_FIXED
```


Belgeyi Extensible Application Markup Language (XAML) biçiminde sabit bir belge olarak kaydeder.

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


Belgeyi Office Open XML SpreadsheetML Belgesi (makro içermeyen) olarak kaydeder.

### XPS {#XPS}
```
public static int XPS
```


Belgeyi XPS (XML Paper Specification) biçiminde kaydeder.

### length {#length}
```
public static int length
```


### fromName(String saveFormatName) {#fromName-java.lang.String}
```
public static int fromName(String saveFormatName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| saveFormatName | java.lang.String |  |

**Returns:**
int
### getName(int saveFormat) {#getName-int}
```
public static String getName(int saveFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
