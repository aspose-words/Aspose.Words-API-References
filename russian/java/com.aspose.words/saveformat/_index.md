---
title: "SaveFormat"
linktitle: "SaveFormat"
second_title: "Aspose.Words для Java"
description: "Указывает формат, в котором документ сохраняется в Java."
type: docs
weight: 595
url: /ru/java/com.aspose.words/saveformat/
---

**Inheritance:**
java.lang.Object
```
public class SaveFormat
```

Указывает формат, в котором сохраняется документ.

 **Examples:** 

Показывает, как преобразовать из DOCX в формат HTML.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 doc.save(getArtifactsDir() + "Document.ConvertToHtml.html", SaveFormat.HTML);
 
```

**M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.SaveFormat)**
## Поля

| Поле | Описание |
| --- | --- |
| [AZW_3](#AZW-3) | Сохраняет документ в формате AZW3. |
| [BMP](#BMP) | Отрисовывает страницу документа и сохраняет её как BMP‑файл. |
| [DOC](#DOC) | Сохраняет документ в формате Microsoft Word 97‑2007 Document. |
| [DOCLING](#DOCLING) | Сохраняет документ в формате Docling JSON. |
| [DOCM](#DOCM) | Сохраняет документ как документ Office Open XML WordprocessingML с поддержкой макросов. |
| [DOCX](#DOCX) | Сохраняет документ как документ Office Open XML WordprocessingML (без макросов). |
| [DOT](#DOT) | Сохраняет документ в формате Microsoft Word 97‑2007 Template. |
| [DOTM](#DOTM) | Сохраняет документ как шаблон Office Open XML WordprocessingML с поддержкой макросов. |
| [DOTX](#DOTX) | Сохраняет документ как шаблон Office Open XML WordprocessingML (без макросов). |
| [EMF](#EMF) | Отрисовывает страницу документа и сохраняет её как векторный файл EMF (Enhanced Meta File). |
| [EPS](#EPS) | Отрисовывает страницу документа и сохраняет её как EPS‑файл. |
| [EPUB](#EPUB) | Сохраняет документ в формате EPUB. |
| [FLAT_OPC](#FLAT-OPC) | Сохраняет документ как Office Open XML WordprocessingML, хранящийся в плоском XML‑файле вместо ZIP‑пакета. |
| [FLAT_OPC_MACRO_ENABLED](#FLAT-OPC-MACRO-ENABLED) | Сохраняет документ как Office Open XML WordprocessingML с поддержкой макросов, хранящийся в плоском XML‑файле вместо ZIP‑пакета. |
| [FLAT_OPC_TEMPLATE](#FLAT-OPC-TEMPLATE) | Сохраняет документ как шаблон Office Open XML WordprocessingML (без макросов), хранящийся в плоском XML‑файле вместо ZIP‑пакета. |
| [FLAT_OPC_TEMPLATE_MACRO_ENABLED](#FLAT-OPC-TEMPLATE-MACRO-ENABLED) | Сохраняет документ как шаблон Office Open XML WordprocessingML с поддержкой макросов, хранящийся в плоском XML‑файле вместо ZIP‑пакета. |
| [GIF](#GIF) | Отрисовывает страницу документа и сохраняет её в файл GIF. |
| [HTML](#HTML) | Сохраняет документ в формате HTML. |
| [HTML_FIXED](#HTML-FIXED) | Сохраняет документ в формате HTML, используя абсолютно позиционированные элементы |
| [JPEG](#JPEG) | Отрисовывает страницу документа и сохраняет её в файл JPEG. |
| [MARKDOWN](#MARKDOWN) | Сохраняет документ в формате Markdown. |
| [MHTML](#MHTML) | Сохраняет документ в формате MHTML (веб‑архив). |
| [MOBI](#MOBI) | Сохраняет документ в формате MOBI. |
| [ODT](#ODT) | Сохраняет документ как текстовый документ ODF. |
| [OPEN_XPS](#OPEN-XPS) | Сохраняет документ в формате OpenXPS (Ecma‑388). |
| [OTT](#OTT) | Сохраняет документ как шаблон текстового документа ODF. |
| [PCL](#PCL) | Сохраняет документ в формате PCL (Printer Control Language). |
| [PDF](#PDF) | Сохраняет документ в формате PDF (Adobe Portable Document). |
| [PNG](#PNG) | Отрисовывает страницу документа и сохраняет её в файл PNG. |
| [PS](#PS) | Сохраняет документ в формате PS (PostScript). |
| [RTF](#RTF) | Сохраняет документ в формате RTF. |
| [SVG](#SVG) | Сохраняет документ в формате SVG (Scalable Vector Graphics). |
| [TEXT](#TEXT) | Сохраняет документ в формате обычного текста. |
| [TIFF](#TIFF) | Отрисовывает одну или несколько страниц документа и сохраняет их в один многостраничный файл TIFF. |
| [UNKNOWN](#UNKNOWN) | По умолчанию, недопустимое значение формата файла. |
| [WEB_P](#WEB-P) | Отрисовывает страницу документа и сохраняет её в файл WebP. |
| [WORD_ML](#WORD-ML) | Сохраняет документ в формате Microsoft Word 2003 WordprocessingML. |
| [XAML_FIXED](#XAML-FIXED) | Сохраняет документ в формате Extensible Application Markup Language (XAML) как фиксированный документ. |
| [XAML_FLOW](#XAML-FLOW) | **Beta.** Сохраняет документ в формате Extensible Application Markup Language (XAML) как потоковый документ. |
| [XAML_FLOW_PACK](#XAML-FLOW-PACK) | **Beta.** Сохраняет документ в формате пакета Extensible Application Markup Language (XAML) как потоковый документ. |
| [XLSX](#XLSX) | Сохраняет документ как документ Office Open XML SpreadsheetML (без макросов). |
| [XPS](#XPS) | Сохраняет документ в формате XPS (XML Paper Specification). |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String saveFormatName)](#fromName-java.lang.String) |  |
| [getName(int saveFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int saveFormat)](#toString-int) |  |
### AZW_3 {#AZW-3}
```
public static int AZW_3
```


Сохраняет документ в формате AZW3.

### BMP {#BMP}
```
public static int BMP
```


Отрисовывает страницу документа и сохраняет её как BMP‑файл.

### DOC {#DOC}
```
public static int DOC
```


Сохраняет документ в формате Microsoft Word 97‑2007 Document.

### DOCLING {#DOCLING}
```
public static int DOCLING
```


Сохраняет документ в формате Docling JSON.

### DOCM {#DOCM}
```
public static int DOCM
```


Сохраняет документ как документ Office Open XML WordprocessingML с поддержкой макросов.

### DOCX {#DOCX}
```
public static int DOCX
```


Сохраняет документ как документ Office Open XML WordprocessingML (без макросов).

### DOT {#DOT}
```
public static int DOT
```


Сохраняет документ в формате Microsoft Word 97‑2007 Template.

### DOTM {#DOTM}
```
public static int DOTM
```


Сохраняет документ как шаблон Office Open XML WordprocessingML с поддержкой макросов.

### DOTX {#DOTX}
```
public static int DOTX
```


Сохраняет документ как шаблон Office Open XML WordprocessingML (без макросов).

### EMF {#EMF}
```
public static int EMF
```


Отрисовывает страницу документа и сохраняет её как векторный файл EMF (Enhanced Meta File).

### EPS {#EPS}
```
public static int EPS
```


Отрисовывает страницу документа и сохраняет её как EPS‑файл.

### EPUB {#EPUB}
```
public static int EPUB
```


Сохраняет документ в формате EPUB.

### FLAT_OPC {#FLAT-OPC}
```
public static int FLAT_OPC
```


Сохраняет документ как Office Open XML WordprocessingML, хранящийся в плоском XML‑файле вместо ZIP‑пакета.

### FLAT_OPC_MACRO_ENABLED {#FLAT-OPC-MACRO-ENABLED}
```
public static int FLAT_OPC_MACRO_ENABLED
```


Сохраняет документ как Office Open XML WordprocessingML с поддержкой макросов, хранящийся в плоском XML‑файле вместо ZIP‑пакета.

### FLAT_OPC_TEMPLATE {#FLAT-OPC-TEMPLATE}
```
public static int FLAT_OPC_TEMPLATE
```


Сохраняет документ как шаблон Office Open XML WordprocessingML (без макросов), хранящийся в плоском XML‑файле вместо ZIP‑пакета.

### FLAT_OPC_TEMPLATE_MACRO_ENABLED {#FLAT-OPC-TEMPLATE-MACRO-ENABLED}
```
public static int FLAT_OPC_TEMPLATE_MACRO_ENABLED
```


Сохраняет документ как шаблон Office Open XML WordprocessingML с поддержкой макросов, хранящийся в плоском XML‑файле вместо ZIP‑пакета.

### GIF {#GIF}
```
public static int GIF
```


Отрисовывает страницу документа и сохраняет её в файл GIF.

### HTML {#HTML}
```
public static int HTML
```


Сохраняет документ в формате HTML.

### HTML_FIXED {#HTML-FIXED}
```
public static int HTML_FIXED
```


Сохраняет документ в формате HTML, используя абсолютно позиционированные элементы

### JPEG {#JPEG}
```
public static int JPEG
```


Отрисовывает страницу документа и сохраняет её в файл JPEG.

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


Сохраняет документ в формате Markdown.

### MHTML {#MHTML}
```
public static int MHTML
```


Сохраняет документ в формате MHTML (веб‑архив).

### MOBI {#MOBI}
```
public static int MOBI
```


Сохраняет документ в формате MOBI.

### ODT {#ODT}
```
public static int ODT
```


Сохраняет документ как текстовый документ ODF.

### OPEN_XPS {#OPEN-XPS}
```
public static int OPEN_XPS
```


Сохраняет документ в формате OpenXPS (Ecma‑388).

### OTT {#OTT}
```
public static int OTT
```


Сохраняет документ как шаблон текстового документа ODF.

### PCL {#PCL}
```
public static int PCL
```


Сохраняет документ в формате PCL (Printer Control Language).

### PDF {#PDF}
```
public static int PDF
```


Сохраняет документ в формате PDF (Adobe Portable Document).

### PNG {#PNG}
```
public static int PNG
```


Отрисовывает страницу документа и сохраняет её в файл PNG.

### PS {#PS}
```
public static int PS
```


Сохраняет документ в формате PS (PostScript).

### RTF {#RTF}
```
public static int RTF
```


Сохраняет документ в формате RTF. Все символы выше 7‑бит экранируются в виде шестнадцатеричных или Unicode‑символов.

### SVG {#SVG}
```
public static int SVG
```


Сохраняет документ в формате SVG (Scalable Vector Graphics).

### TEXT {#TEXT}
```
public static int TEXT
```


Сохраняет документ в формате обычного текста.

### TIFF {#TIFF}
```
public static int TIFF
```


Отрисовывает одну или несколько страниц документа и сохраняет их в один многостраничный файл TIFF.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


По умолчанию, недопустимое значение формата файла.

### WEB_P {#WEB-P}
```
public static int WEB_P
```


Отрисовывает страницу документа и сохраняет её в файл WebP.

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


Сохраняет документ в формате Microsoft Word 2003 WordprocessingML.

### XAML_FIXED {#XAML-FIXED}
```
public static int XAML_FIXED
```


Сохраняет документ в формате Extensible Application Markup Language (XAML) как фиксированный документ.

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


Сохраняет документ как документ Office Open XML SpreadsheetML (без макросов).

### XPS {#XPS}
```
public static int XPS
```


Сохраняет документ в формате XPS (XML Paper Specification).

### length {#length}
```
public static int length
```


### fromName(String saveFormatName) {#fromName-java.lang.String}
```
public static int fromName(String saveFormatName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| saveFormatName | java.lang.String |  |

**Returns:**
int
### getName(int saveFormat) {#getName-int}
```
public static String getName(int saveFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
