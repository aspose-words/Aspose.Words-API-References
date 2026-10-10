---
title: "LoadFormat"
linktitle: "LoadFormat"
second_title: "Aspose.Words per Java"
description: "Indica il formato del documento da caricare in Java."
type: docs
weight: 434
url: /it/java/com.aspose.words/loadformat/
---

**Inheritance:**
java.lang.Object
```
public class LoadFormat
```

Indica il formato del documento da caricare.

 **Examples:** 

Mostra come inserire il contenuto HTML da una pagina web in un nuovo documento.

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

Mostra come utilizzare i metodi di FileFormatUtil per rilevare il formato di un documento.

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

Mostra come specificare un URI di base quando si apre un documento html.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [AUTO](#AUTO) | Istruisce Aspose.Words a riconoscere automaticamente il formato. |
| [AZW_3](#AZW-3) | Formato AZW3. |
| [CHM](#CHM) | Formato CHM (Compiled HTML Help). |
| [DOC](#DOC) | Documento Microsoft Word 95 o Word 97 - 2003. |
| [DOCM](#DOCM) | Documento Office Open XML WordprocessingML con macro. |
| [DOCX](#DOCX) | Documento Office Open XML WordprocessingML (senza macro). |
| [DOC_PRE_WORD_60](#DOC-PRE-WORD-60) | Il documento è in formato pre-Word 95. |
| [DOT](#DOT) | Modello Microsoft Word 95 o Word 97 - 2003. |
| [DOTM](#DOTM) | Modello Office Open XML WordprocessingML con macro. |
| [DOTX](#DOTX) | Modello Office Open XML WordprocessingML (senza macro). |
| [EPUB](#EPUB) | Formato EPUB. |
| [FLAT_OPC](#FLAT-OPC) | Office Open XML WordprocessingML memorizzato in un file XML piatto invece di un pacchetto ZIP. |
| [FLAT_OPC_MACRO_ENABLED](#FLAT-OPC-MACRO-ENABLED) | Documento Office Open XML WordprocessingML con macro memorizzato in un file XML piatto anziché in un pacchetto ZIP. |
| [FLAT_OPC_TEMPLATE](#FLAT-OPC-TEMPLATE) | Modello Office Open XML WordprocessingML (senza macro) memorizzato in un file XML piatto anziché in un pacchetto ZIP. |
| [FLAT_OPC_TEMPLATE_MACRO_ENABLED](#FLAT-OPC-TEMPLATE-MACRO-ENABLED) | Modello Office Open XML WordprocessingML con macro memorizzato in un file XML piatto anziché in un pacchetto ZIP. |
| [HTML](#HTML) | Formato HTML. |
| [MARKDOWN](#MARKDOWN) | Documento di testo Markdown. |
| [MHTML](#MHTML) | Formato MHTML (archivio Web). |
| [MOBI](#MOBI) | Formato MOBI. |
| [MS_WORKS](#MS-WORKS) | Documento Microsoft Works 8. |
| [ODT](#ODT) | Documento di testo ODF. |
| [OTT](#OTT) | Modello di documento di testo ODF. |
| [PDF](#PDF) | Documento PDF. |
| [RTF](#RTF) | Formato RTF. |
| [TEXT](#TEXT) | Testo semplice. |
| [UNKNOWN](#UNKNOWN) | Formato non riconosciuto, impossibile da caricare con Aspose.Words. |
| [WORD_ML](#WORD-ML) | Formato Microsoft Word 2003 WordprocessingML. |
| [XML](#XML) | Documento XML. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String loadFormatName)](#fromName-java.lang.String) |  |
| [getName(int loadFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int loadFormat)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Istruisce Aspose.Words a riconoscere automaticamente il formato.

### AZW_3 {#AZW-3}
```
public static int AZW_3
```


Formato AZW3. Utilizzato dai lettori Amazon Kindle.

### CHM {#CHM}
```
public static int CHM
```


Formato CHM (Compiled HTML Help).

### DOC {#DOC}
```
public static int DOC
```


Documento Microsoft Word 95 o Word 97 - 2003.

### DOCM {#DOCM}
```
public static int DOCM
```


Documento Office Open XML WordprocessingML con macro.

### DOCX {#DOCX}
```
public static int DOCX
```


Documento Office Open XML WordprocessingML (senza macro).

### DOC_PRE_WORD_60 {#DOC-PRE-WORD-60}
```
public static int DOC_PRE_WORD_60
```


Il documento è in formato pre-Word 95. Aspose.Words attualmente non supporta il caricamento di tali documenti.

### DOT {#DOT}
```
public static int DOT
```


Modello Microsoft Word 95 o Word 97 - 2003.

### DOTM {#DOTM}
```
public static int DOTM
```


Modello Office Open XML WordprocessingML con macro.

### DOTX {#DOTX}
```
public static int DOTX
```


Modello Office Open XML WordprocessingML (senza macro).

### EPUB {#EPUB}
```
public static int EPUB
```


Formato EPUB.

### FLAT_OPC {#FLAT-OPC}
```
public static int FLAT_OPC
```


Office Open XML WordprocessingML memorizzato in un file XML piatto invece di un pacchetto ZIP.

### FLAT_OPC_MACRO_ENABLED {#FLAT-OPC-MACRO-ENABLED}
```
public static int FLAT_OPC_MACRO_ENABLED
```


Documento Office Open XML WordprocessingML con macro memorizzato in un file XML piatto anziché in un pacchetto ZIP.

### FLAT_OPC_TEMPLATE {#FLAT-OPC-TEMPLATE}
```
public static int FLAT_OPC_TEMPLATE
```


Modello Office Open XML WordprocessingML (senza macro) memorizzato in un file XML piatto anziché in un pacchetto ZIP.

### FLAT_OPC_TEMPLATE_MACRO_ENABLED {#FLAT-OPC-TEMPLATE-MACRO-ENABLED}
```
public static int FLAT_OPC_TEMPLATE_MACRO_ENABLED
```


Modello Office Open XML WordprocessingML con macro memorizzato in un file XML piatto anziché in un pacchetto ZIP.

### HTML {#HTML}
```
public static int HTML
```


Formato HTML.

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


Documento di testo Markdown.

### MHTML {#MHTML}
```
public static int MHTML
```


Formato MHTML (archivio Web).

### MOBI {#MOBI}
```
public static int MOBI
```


Formato MOBI. Utilizzato dal lettore MobiPocket e dai lettori Amazon Kindle.

### MS_WORKS {#MS-WORKS}
```
public static int MS_WORKS
```


Documento Microsoft Works 8.

### ODT {#ODT}
```
public static int ODT
```


Documento di testo ODF.

### OTT {#OTT}
```
public static int OTT
```


Modello di documento di testo ODF.

### PDF {#PDF}
```
public static int PDF
```


Documento PDF.

### RTF {#RTF}
```
public static int RTF
```


Formato RTF.

### TEXT {#TEXT}
```
public static int TEXT
```


Testo semplice.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Formato non riconosciuto, impossibile da caricare con Aspose.Words.

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


Formato Microsoft Word 2003 WordprocessingML.

### XML {#XML}
```
public static int XML
```


Documento XML.

### length {#length}
```
public static int length
```


### fromName(String loadFormatName) {#fromName-java.lang.String}
```
public static int fromName(String loadFormatName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| loadFormatName | java.lang.String |  |

**Returns:**
int
### getName(int loadFormat) {#getName-int}
```
public static String getName(int loadFormat)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| loadFormat | int |  |

**Returns:**
java.lang.String
