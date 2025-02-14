---
title: LoadFormat
linktitle: LoadFormat
second_title: Aspose.Words for Java
description: Indicates the format of the document that is to be loaded in Java.
type: docs
weight: 426
url: /java/com.aspose.words/loadformat/
---

**Inheritance:**
java.lang.Object
```
public class LoadFormat
```

Indicates the format of the document that is to be loaded.

 **Examples:** 

Shows how to specify a base URI when opening an html document.

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

Shows how to insert the HTML contents from a web page into a new document.

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

Shows how to use the FileFormatUtil methods to detect the format of a document.

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
## Fields

| Field | Description |
| --- | --- |
| [AUTO](#AUTO) | Instructs Aspose.Words to recognize the format automatically. |
| [AZW_3](#AZW-3) | AZW3 format. |
| [CHM](#CHM) | CHM (Compiled HTML Help) format. |
| [DOC](#DOC) | Microsoft Word 95 or Word 97 - 2003 Document. |
| [DOCM](#DOCM) | Office Open XML WordprocessingML Macro-Enabled Document. |
| [DOCX](#DOCX) | Office Open XML WordprocessingML Document (macro-free). |
| [DOC_PRE_WORD_60](#DOC-PRE-WORD-60) | The document is in pre-Word 95 format. |
| [DOT](#DOT) | Microsoft Word 95 or Word 97 - 2003 Template. |
| [DOTM](#DOTM) | Office Open XML WordprocessingML Macro-Enabled Template. |
| [DOTX](#DOTX) | Office Open XML WordprocessingML Template (macro-free). |
| [EPUB](#EPUB) | EPUB format. |
| [FLAT_OPC](#FLAT-OPC) | Office Open XML WordprocessingML stored in a flat XML file instead of a ZIP package. |
| [FLAT_OPC_MACRO_ENABLED](#FLAT-OPC-MACRO-ENABLED) | Office Open XML WordprocessingML Macro-Enabled Document stored in a flat XML file instead of a ZIP package. |
| [FLAT_OPC_TEMPLATE](#FLAT-OPC-TEMPLATE) | Office Open XML WordprocessingML Template (macro-free) stored in a flat XML file instead of a ZIP package. |
| [FLAT_OPC_TEMPLATE_MACRO_ENABLED](#FLAT-OPC-TEMPLATE-MACRO-ENABLED) | Office Open XML WordprocessingML Macro-Enabled Template stored in a flat XML file instead of a ZIP package. |
| [HTML](#HTML) | HTML format. |
| [MARKDOWN](#MARKDOWN) | Markdown text document. |
| [MHTML](#MHTML) | MHTML (Web archive) format. |
| [MOBI](#MOBI) | MOBI format. |
| [MS_WORKS](#MS-WORKS) | Microsoft Works 8 Document. |
| [ODT](#ODT) | ODF Text Document. |
| [OTT](#OTT) | ODF Text Document Template. |
| [PDF](#PDF) | Pdf document. |
| [RTF](#RTF) | RTF format. |
| [TEXT](#TEXT) | Plain Text. |
| [UNKNOWN](#UNKNOWN) | Unrecognized format, cannot be loaded by Aspose.Words. |
| [WORD_ML](#WORD-ML) | Microsoft Word 2003 WordprocessingML format. |
| [XML](#XML) | XML document. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String loadFormatName)](#fromName-java.lang.String) |  |
| [getName(int loadFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int loadFormat)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Instructs Aspose.Words to recognize the format automatically.

### AZW_3 {#AZW-3}
```
public static int AZW_3
```


AZW3 format. Used by Amazon Kindle readers.

### CHM {#CHM}
```
public static int CHM
```


CHM (Compiled HTML Help) format.

### DOC {#DOC}
```
public static int DOC
```


Microsoft Word 95 or Word 97 - 2003 Document.

### DOCM {#DOCM}
```
public static int DOCM
```


Office Open XML WordprocessingML Macro-Enabled Document.

### DOCX {#DOCX}
```
public static int DOCX
```


Office Open XML WordprocessingML Document (macro-free).

### DOC_PRE_WORD_60 {#DOC-PRE-WORD-60}
```
public static int DOC_PRE_WORD_60
```


The document is in pre-Word 95 format. Aspose.Words does not currently support loading such documents.

### DOT {#DOT}
```
public static int DOT
```


Microsoft Word 95 or Word 97 - 2003 Template.

### DOTM {#DOTM}
```
public static int DOTM
```


Office Open XML WordprocessingML Macro-Enabled Template.

### DOTX {#DOTX}
```
public static int DOTX
```


Office Open XML WordprocessingML Template (macro-free).

### EPUB {#EPUB}
```
public static int EPUB
```


EPUB format.

### FLAT_OPC {#FLAT-OPC}
```
public static int FLAT_OPC
```


Office Open XML WordprocessingML stored in a flat XML file instead of a ZIP package.

### FLAT_OPC_MACRO_ENABLED {#FLAT-OPC-MACRO-ENABLED}
```
public static int FLAT_OPC_MACRO_ENABLED
```


Office Open XML WordprocessingML Macro-Enabled Document stored in a flat XML file instead of a ZIP package.

### FLAT_OPC_TEMPLATE {#FLAT-OPC-TEMPLATE}
```
public static int FLAT_OPC_TEMPLATE
```


Office Open XML WordprocessingML Template (macro-free) stored in a flat XML file instead of a ZIP package.

### FLAT_OPC_TEMPLATE_MACRO_ENABLED {#FLAT-OPC-TEMPLATE-MACRO-ENABLED}
```
public static int FLAT_OPC_TEMPLATE_MACRO_ENABLED
```


Office Open XML WordprocessingML Macro-Enabled Template stored in a flat XML file instead of a ZIP package.

### HTML {#HTML}
```
public static int HTML
```


HTML format.

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


Markdown text document.

### MHTML {#MHTML}
```
public static int MHTML
```


MHTML (Web archive) format.

### MOBI {#MOBI}
```
public static int MOBI
```


MOBI format. Used by MobiPocket reader and Amazon Kindle readers.

### MS_WORKS {#MS-WORKS}
```
public static int MS_WORKS
```


Microsoft Works 8 Document.

### ODT {#ODT}
```
public static int ODT
```


ODF Text Document.

### OTT {#OTT}
```
public static int OTT
```


ODF Text Document Template.

### PDF {#PDF}
```
public static int PDF
```


Pdf document.

### RTF {#RTF}
```
public static int RTF
```


RTF format.

### TEXT {#TEXT}
```
public static int TEXT
```


Plain Text.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Unrecognized format, cannot be loaded by Aspose.Words.

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


Microsoft Word 2003 WordprocessingML format.

### XML {#XML}
```
public static int XML
```


XML document.

### length {#length}
```
public static int length
```


### fromName(String loadFormatName) {#fromName-java.lang.String}
```
public static int fromName(String loadFormatName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| loadFormatName | java.lang.String |  |

**Returns:**
int
### getName(int loadFormat) {#getName-int}
```
public static String getName(int loadFormat)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| loadFormat | int |  |

**Returns:**
java.lang.String
