---
title: "LoadFormat"
linktitle: "LoadFormat"
second_title: "Aspose.Words для Java"
description: "Указывает формат документа, который будет загружен в Java."
type: docs
weight: 434
url: /ru/java/com.aspose.words/loadformat/
---

**Inheritance:**
java.lang.Object
```
public class LoadFormat
```

Указывает формат документа, который будет загружен.

 **Examples:** 

Показывает, как вставить HTML‑содержимое веб‑страницы в новый документ.

```

 URL url = new URL("https://www.aspose.com");

 // The easiest way to load our document from the internet is make use of the URLConnection class.
 URLConnection webClient = url.openConnection();

 // Download the bytes from the location referenced by the URL.
 InputStream inputStream = webClient.getInputStream();

 // Convert the input stream to a byte array.
 int pos;
 ByteArrayOutputStream bos = new ByteArrayOutputStream();
 while ((pos = inputStream.read()) != -1) bos.write(pos);

 byte[] dataBytes = bos.toByteArray();

 // Wrap the bytes representing the document in memory into a stream object.
 ByteArrayInputStream byteStream = new ByteArrayInputStream(dataBytes);

 // The baseUri property should be set to ensure any relative img paths are retrieved correctly.
 LoadOptions options = new LoadOptions(LoadFormat.HTML, "", url.getPath());

 // Load the HTML document from stream and pass the LoadOptions object.
 Document doc = new Document(byteStream, options);

 doc.save(getArtifactsDir() + "Document.InsertHtmlFromWebPage.docx");
 
```

Показывает, как использовать методы FileFormatUtil для определения формата документа.

```

 // Load a document from a file that is missing a file extension, and then detect its file format.
 FileInputStream docStream = new FileInputStream(getMyDir() + "Word document with missing file extension");

 FileFormatInfo info = FileFormatUtil.detectFileFormat(docStream);

 int loadFormat = info.getLoadFormat();

 Assert.assertEquals(LoadFormat.DOC, loadFormat);

 // Below are two methods of converting a LoadFormat to its corresponding SaveFormat.
 // 1 -  Get the file extension string for the LoadFormat, then get the corresponding SaveFormat from that string:
 String fileExtension = FileFormatUtil.loadFormatToExtension(loadFormat);

 int saveFormat = FileFormatUtil.extensionToSaveFormat(fileExtension);

 // 2 -  Convert the LoadFormat directly to its SaveFormat:
 saveFormat = FileFormatUtil.loadFormatToSaveFormat(loadFormat);

 // Load a document from the stream, and then save it to the automatically detected file extension.
 Document doc = new Document(docStream);

 Assert.assertEquals(".doc", FileFormatUtil.saveFormatToExtension(saveFormat));

 doc.save(getArtifactsDir() + "File.SaveToDetectedFileFormat" + FileFormatUtil.saveFormatToExtension(saveFormat));
 
```

Показывает, как указать базовый URI при открытии HTML‑документа.

```

 // Suppose we want to load an .html document that contains an image linked by a relative URI
 // while the image is in a different location. In that case, we will need to resolve the relative URI into an absolute one.
 // We can provide a base URI using an HtmlLoadOptions object.
 HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.HTML, "", getImageDir());

 Assert.assertEquals(LoadFormat.HTML, loadOptions.getLoadFormat());

 Document doc = new Document(getMyDir() + "Missing image.html", loadOptions);

 // While the image was broken in the input .html, our custom base URI helped us repair the link.
 Shape imageShape = (Shape) doc.getChildNodes(NodeType.SHAPE, true).get(0);
 Assert.assertTrue(imageShape.isImage());

 // This output document will display the image that was missing.
 doc.save(getArtifactsDir() + "HtmlLoadOptions.BaseUri.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [AUTO](#AUTO) | Инструктирует Aspose.Words автоматически распознавать формат. |
| [AZW_3](#AZW-3) | Формат AZW3. |
| [CHM](#CHM) | Формат CHM (Compiled HTML Help). |
| [DOC](#DOC) | Документ Microsoft Word 95 или Word 97‑2003. |
| [DOCM](#DOCM) | Документ Office Open XML WordprocessingML с поддержкой макросов. |
| [DOCX](#DOCX) | Документ Office Open XML WordprocessingML (без макросов). |
| [DOC_PRE_WORD_60](#DOC-PRE-WORD-60) | Документ в формате до Word 95. |
| [DOT](#DOT) | Шаблон Microsoft Word 95 или Word 97‑2003. |
| [DOTM](#DOTM) | Шаблон Office Open XML WordprocessingML с поддержкой макросов. |
| [DOTX](#DOTX) | Шаблон Office Open XML WordprocessingML (без макросов). |
| [EPUB](#EPUB) | Формат EPUB. |
| [FLAT_OPC](#FLAT-OPC) | Office Open XML WordprocessingML, хранящийся в плоском XML‑файле вместо ZIP‑пакета. |
| [FLAT_OPC_MACRO_ENABLED](#FLAT-OPC-MACRO-ENABLED) | Документ Office Open XML WordprocessingML с поддержкой макросов, сохранённый в плоском XML‑файле вместо ZIP‑пакета. |
| [FLAT_OPC_TEMPLATE](#FLAT-OPC-TEMPLATE) | Шаблон Office Open XML WordprocessingML (без макросов), сохранённый в плоском XML‑файле вместо ZIP‑пакета. |
| [FLAT_OPC_TEMPLATE_MACRO_ENABLED](#FLAT-OPC-TEMPLATE-MACRO-ENABLED) | Шаблон Office Open XML WordprocessingML с поддержкой макросов, сохранённый в плоском XML‑файле вместо ZIP‑пакета. |
| [HTML](#HTML) | Формат HTML. |
| [MARKDOWN](#MARKDOWN) | Текстовый документ Markdown. |
| [MHTML](#MHTML) | Формат MHTML (веб‑архив). |
| [MOBI](#MOBI) | Формат MOBI. |
| [MS_WORKS](#MS-WORKS) | Документ Microsoft Works 8. |
| [ODT](#ODT) | Текстовый документ ODF. |
| [OTT](#OTT) | Шаблон текстового документа ODF. |
| [PDF](#PDF) | Документ PDF. |
| [RTF](#RTF) | Формат RTF. |
| [TEXT](#TEXT) | Простой текст. |
| [UNKNOWN](#UNKNOWN) | Неизвестный формат, невозможно загрузить с помощью Aspose.Words. |
| [WORD_ML](#WORD-ML) | Формат Microsoft Word 2003 WordprocessingML. |
| [XML](#XML) | XML‑документ. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String loadFormatName)](#fromName-java.lang.String) |  |
| [getName(int loadFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int loadFormat)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Инструктирует Aspose.Words автоматически распознавать формат.

### AZW_3 {#AZW-3}
```
public static int AZW_3
```


Формат AZW3. Используется в устройствах Amazon Kindle.

### CHM {#CHM}
```
public static int CHM
```


Формат CHM (Compiled HTML Help).

### DOC {#DOC}
```
public static int DOC
```


Документ Microsoft Word 95 или Word 97‑2003.

### DOCM {#DOCM}
```
public static int DOCM
```


Документ Office Open XML WordprocessingML с поддержкой макросов.

### DOCX {#DOCX}
```
public static int DOCX
```


Документ Office Open XML WordprocessingML (без макросов).

### DOC_PRE_WORD_60 {#DOC-PRE-WORD-60}
```
public static int DOC_PRE_WORD_60
```


Документ в формате до Word 95. В настоящее время Aspose.Words не поддерживает загрузку таких документов.

### DOT {#DOT}
```
public static int DOT
```


Шаблон Microsoft Word 95 или Word 97‑2003.

### DOTM {#DOTM}
```
public static int DOTM
```


Шаблон Office Open XML WordprocessingML с поддержкой макросов.

### DOTX {#DOTX}
```
public static int DOTX
```


Шаблон Office Open XML WordprocessingML (без макросов).

### EPUB {#EPUB}
```
public static int EPUB
```


Формат EPUB.

### FLAT_OPC {#FLAT-OPC}
```
public static int FLAT_OPC
```


Office Open XML WordprocessingML, хранящийся в плоском XML‑файле вместо ZIP‑пакета.

### FLAT_OPC_MACRO_ENABLED {#FLAT-OPC-MACRO-ENABLED}
```
public static int FLAT_OPC_MACRO_ENABLED
```


Документ Office Open XML WordprocessingML с поддержкой макросов, сохранённый в плоском XML‑файле вместо ZIP‑пакета.

### FLAT_OPC_TEMPLATE {#FLAT-OPC-TEMPLATE}
```
public static int FLAT_OPC_TEMPLATE
```


Шаблон Office Open XML WordprocessingML (без макросов), сохранённый в плоском XML‑файле вместо ZIP‑пакета.

### FLAT_OPC_TEMPLATE_MACRO_ENABLED {#FLAT-OPC-TEMPLATE-MACRO-ENABLED}
```
public static int FLAT_OPC_TEMPLATE_MACRO_ENABLED
```


Шаблон Office Open XML WordprocessingML с поддержкой макросов, сохранённый в плоском XML‑файле вместо ZIP‑пакета.

### HTML {#HTML}
```
public static int HTML
```


Формат HTML.

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


Текстовый документ Markdown.

### MHTML {#MHTML}
```
public static int MHTML
```


Формат MHTML (веб‑архив).

### MOBI {#MOBI}
```
public static int MOBI
```


Формат MOBI. Используется в читалках MobiPocket и Amazon Kindle.

### MS_WORKS {#MS-WORKS}
```
public static int MS_WORKS
```


Документ Microsoft Works 8.

### ODT {#ODT}
```
public static int ODT
```


Текстовый документ ODF.

### OTT {#OTT}
```
public static int OTT
```


Шаблон текстового документа ODF.

### PDF {#PDF}
```
public static int PDF
```


Документ PDF.

### RTF {#RTF}
```
public static int RTF
```


Формат RTF.

### TEXT {#TEXT}
```
public static int TEXT
```


Простой текст.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Неизвестный формат, невозможно загрузить с помощью Aspose.Words.

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


Формат Microsoft Word 2003 WordprocessingML.

### XML {#XML}
```
public static int XML
```


XML‑документ.

### length {#length}
```
public static int length
```


### fromName(String loadFormatName) {#fromName-java.lang.String}
```
public static int fromName(String loadFormatName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| loadFormatName | java.lang.String |  |

**Returns:**
int
### getName(int loadFormat) {#getName-int}
```
public static String getName(int loadFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| loadFormat | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int loadFormat) {#toString-int}
```
public static String toString(int loadFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| loadFormat | int |  |

**Returns:**
java.lang.String
