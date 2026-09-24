---
title: "LoadFormat"
linktitle: "LoadFormat"
second_title: "Aspose.Words para Java"
description: "Indica el formato del documento que se debe cargar en Java."
type: docs
weight: 434
url: /es/java/com.aspose.words/loadformat/
---

**Inheritance:**
java.lang.Object
```
public class LoadFormat
```

Indica el formato del documento que se va a cargar.

 **Examples:** 

Muestra cómo insertar el contenido HTML de una página web en un nuevo documento.

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

Muestra cómo usar los métodos de FileFormatUtil para detectar el formato de un documento.

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

Muestra cómo especificar una URI base al abrir un documento html.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [AUTO](#AUTO) | Indica a Aspose.Words que reconozca el formato automáticamente. |
| [AZW_3](#AZW-3) | Formato AZW3. |
| [CHM](#CHM) | Formato CHM (Ayuda HTML compilada). |
| [DOC](#DOC) | Documento Microsoft Word 95 o Word 97 - 2003. |
| [DOCM](#DOCM) | Documento Office Open XML WordprocessingML con macros habilitadas. |
| [DOCX](#DOCX) | Documento Office Open XML WordprocessingML (sin macros). |
| [DOC_PRE_WORD_60](#DOC-PRE-WORD-60) | El documento está en formato pre-Word 95. |
| [DOT](#DOT) | Plantilla Microsoft Word 95 o Word 97 - 2003. |
| [DOTM](#DOTM) | Plantilla Office Open XML WordprocessingML con macros habilitadas. |
| [DOTX](#DOTX) | Plantilla Office Open XML WordprocessingML (sin macros). |
| [EPUB](#EPUB) | Formato EPUB. |
| [FLAT_OPC](#FLAT-OPC) | Office Open XML WordprocessingML almacenado en un archivo XML plano en lugar de un paquete ZIP. |
| [FLAT_OPC_MACRO_ENABLED](#FLAT-OPC-MACRO-ENABLED) | Documento de Office Open XML WordprocessingML con macros almacenado en un archivo XML plano en lugar de un paquete ZIP. |
| [FLAT_OPC_TEMPLATE](#FLAT-OPC-TEMPLATE) | Plantilla de Office Open XML WordprocessingML (sin macros) almacenada en un archivo XML plano en lugar de un paquete ZIP. |
| [FLAT_OPC_TEMPLATE_MACRO_ENABLED](#FLAT-OPC-TEMPLATE-MACRO-ENABLED) | Plantilla de Office Open XML WordprocessingML con macros almacenada en un archivo XML plano en lugar de un paquete ZIP. |
| [HTML](#HTML) | Formato HTML. |
| [MARKDOWN](#MARKDOWN) | Documento de texto Markdown. |
| [MHTML](#MHTML) | Formato MHTML (archivo web). |
| [MOBI](#MOBI) | Formato MOBI. |
| [MS_WORKS](#MS-WORKS) | Documento Microsoft Works 8. |
| [ODT](#ODT) | Documento de texto ODF. |
| [OTT](#OTT) | Plantilla de documento de texto ODF. |
| [PDF](#PDF) | Documento PDF. |
| [RTF](#RTF) | Formato RTF. |
| [TEXT](#TEXT) | Texto plano. |
| [UNKNOWN](#UNKNOWN) | Formato no reconocido, no se puede cargar con Aspose.Words. |
| [WORD_ML](#WORD-ML) | Formato Microsoft Word 2003 WordprocessingML. |
| [XML](#XML) | Documento XML. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String loadFormatName)](#fromName-java.lang.String) |  |
| [getName(int loadFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int loadFormat)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Indica a Aspose.Words que reconozca el formato automáticamente.

### AZW_3 {#AZW-3}
```
public static int AZW_3
```


Formato AZW3. Utilizado por los lectores Amazon Kindle.

### CHM {#CHM}
```
public static int CHM
```


Formato CHM (Ayuda HTML compilada).

### DOC {#DOC}
```
public static int DOC
```


Documento Microsoft Word 95 o Word 97 - 2003.

### DOCM {#DOCM}
```
public static int DOCM
```


Documento Office Open XML WordprocessingML con macros habilitadas.

### DOCX {#DOCX}
```
public static int DOCX
```


Documento Office Open XML WordprocessingML (sin macros).

### DOC_PRE_WORD_60 {#DOC-PRE-WORD-60}
```
public static int DOC_PRE_WORD_60
```


El documento está en formato anterior a Word 95. Aspose.Words actualmente no admite cargar dichos documentos.

### DOT {#DOT}
```
public static int DOT
```


Plantilla Microsoft Word 95 o Word 97 - 2003.

### DOTM {#DOTM}
```
public static int DOTM
```


Plantilla Office Open XML WordprocessingML con macros habilitadas.

### DOTX {#DOTX}
```
public static int DOTX
```


Plantilla Office Open XML WordprocessingML (sin macros).

### EPUB {#EPUB}
```
public static int EPUB
```


Formato EPUB.

### FLAT_OPC {#FLAT-OPC}
```
public static int FLAT_OPC
```


Office Open XML WordprocessingML almacenado en un archivo XML plano en lugar de un paquete ZIP.

### FLAT_OPC_MACRO_ENABLED {#FLAT-OPC-MACRO-ENABLED}
```
public static int FLAT_OPC_MACRO_ENABLED
```


Documento de Office Open XML WordprocessingML con macros almacenado en un archivo XML plano en lugar de un paquete ZIP.

### FLAT_OPC_TEMPLATE {#FLAT-OPC-TEMPLATE}
```
public static int FLAT_OPC_TEMPLATE
```


Plantilla de Office Open XML WordprocessingML (sin macros) almacenada en un archivo XML plano en lugar de un paquete ZIP.

### FLAT_OPC_TEMPLATE_MACRO_ENABLED {#FLAT-OPC-TEMPLATE-MACRO-ENABLED}
```
public static int FLAT_OPC_TEMPLATE_MACRO_ENABLED
```


Plantilla de Office Open XML WordprocessingML con macros almacenada en un archivo XML plano en lugar de un paquete ZIP.

### HTML {#HTML}
```
public static int HTML
```


Formato HTML.

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


Documento de texto Markdown.

### MHTML {#MHTML}
```
public static int MHTML
```


Formato MHTML (archivo web).

### MOBI {#MOBI}
```
public static int MOBI
```


Formato MOBI. Utilizado por el lector MobiPocket y los lectores Amazon Kindle.

### MS_WORKS {#MS-WORKS}
```
public static int MS_WORKS
```


Documento Microsoft Works 8.

### ODT {#ODT}
```
public static int ODT
```


Documento de texto ODF.

### OTT {#OTT}
```
public static int OTT
```


Plantilla de documento de texto ODF.

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


Texto plano.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Formato no reconocido, no se puede cargar con Aspose.Words.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| loadFormatName | java.lang.String |  |

**Returns:**
int
### getName(int loadFormat) {#getName-int}
```
public static String getName(int loadFormat)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| loadFormat | int |  |

**Returns:**
java.lang.String
