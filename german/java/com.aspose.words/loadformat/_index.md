---
title: "LoadFormat"
linktitle: "LoadFormat"
second_title: "Aspose.Words für Java"
description: "Gibt das Format des Dokuments an, das in Java geladen werden soll."
type: docs
weight: 434
url: /de/java/com.aspose.words/loadformat/
---

**Inheritance:**
java.lang.Object
```
public class LoadFormat
```

Gibt das Format des zu ladenden Dokuments an.

 **Examples:** 

Zeigt, wie man die HTML-Inhalte einer Webseite in ein neues Dokument einfügt.

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

Zeigt, wie man die FileFormatUtil-Methoden verwendet, um das Format eines Dokuments zu erkennen.

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

Zeigt, wie man eine Basis‑URI beim Öffnen eines HTML‑Dokuments angibt.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [AUTO](#AUTO) | Weist Aspose.Words an, das Format automatisch zu erkennen. |
| [AZW_3](#AZW-3) | AZW3-Format. |
| [CHM](#CHM) | CHM (Compiled HTML Help)-Format. |
| [DOC](#DOC) | Microsoft Word 95 oder Word 97 - 2003 Dokument. |
| [DOCM](#DOCM) | Office Open XML WordprocessingML Makroaktiviertes Dokument. |
| [DOCX](#DOCX) | Office Open XML WordprocessingML Dokument (makrofrei). |
| [DOC_PRE_WORD_60](#DOC-PRE-WORD-60) | Das Dokument liegt im Vor-Word‑95-Format vor. |
| [DOT](#DOT) | Microsoft Word 95 oder Word 97 - 2003 Vorlage. |
| [DOTM](#DOTM) | Office Open XML WordprocessingML Makroaktivierte Vorlage. |
| [DOTX](#DOTX) | Office Open XML WordprocessingML Vorlage (makrofrei). |
| [EPUB](#EPUB) | EPUB-Format. |
| [FLAT_OPC](#FLAT-OPC) | Office Open XML WordprocessingML, gespeichert in einer flachen XML-Datei anstelle eines ZIP-Pakets. |
| [FLAT_OPC_MACRO_ENABLED](#FLAT-OPC-MACRO-ENABLED) | Office Open XML WordprocessingML Makroaktiviertes Dokument, gespeichert in einer flachen XML-Datei anstelle eines ZIP-Pakets. |
| [FLAT_OPC_TEMPLATE](#FLAT-OPC-TEMPLATE) | Office Open XML WordprocessingML Vorlage (makrofrei) gespeichert in einer flachen XML-Datei anstelle eines ZIP-Pakets. |
| [FLAT_OPC_TEMPLATE_MACRO_ENABLED](#FLAT-OPC-TEMPLATE-MACRO-ENABLED) | Office Open XML WordprocessingML-Makroaktivierte Vorlage gespeichert in einer flachen XML-Datei anstelle eines ZIP-Pakets. |
| [HTML](#HTML) | HTML-Format. |
| [MARKDOWN](#MARKDOWN) | Markdown-Textdokument. |
| [MHTML](#MHTML) | MHTML (Web-Archiv) Format. |
| [MOBI](#MOBI) | MOBI-Format. |
| [MS_WORKS](#MS-WORKS) | Microsoft Works 8 Dokument. |
| [ODT](#ODT) | ODF-Textdokument. |
| [OTT](#OTT) | ODF-Textdokumentvorlage. |
| [PDF](#PDF) | PDF-Dokument. |
| [RTF](#RTF) | RTF-Format. |
| [TEXT](#TEXT) | Klartext. |
| [UNKNOWN](#UNKNOWN) | Unbekanntes Format, kann nicht von Aspose.Words geladen werden. |
| [WORD_ML](#WORD-ML) | Microsoft Word 2003 WordprocessingML-Format. |
| [XML](#XML) | XML-Dokument. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String loadFormatName)](#fromName-java.lang.String) |  |
| [getName(int loadFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int loadFormat)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Weist Aspose.Words an, das Format automatisch zu erkennen.

### AZW_3 {#AZW-3}
```
public static int AZW_3
```


AZW3-Format. Verwendet von Amazon Kindle-Lesegeräten.

### CHM {#CHM}
```
public static int CHM
```


CHM (Compiled HTML Help)-Format.

### DOC {#DOC}
```
public static int DOC
```


Microsoft Word 95 oder Word 97 - 2003 Dokument.

### DOCM {#DOCM}
```
public static int DOCM
```


Office Open XML WordprocessingML Makroaktiviertes Dokument.

### DOCX {#DOCX}
```
public static int DOCX
```


Office Open XML WordprocessingML Dokument (makrofrei).

### DOC_PRE_WORD_60 {#DOC-PRE-WORD-60}
```
public static int DOC_PRE_WORD_60
```


Das Dokument ist im Vor-Word‑95-Format. Aspose.Words unterstützt das Laden solcher Dokumente derzeit nicht.

### DOT {#DOT}
```
public static int DOT
```


Microsoft Word 95 oder Word 97 - 2003 Vorlage.

### DOTM {#DOTM}
```
public static int DOTM
```


Office Open XML WordprocessingML Makroaktivierte Vorlage.

### DOTX {#DOTX}
```
public static int DOTX
```


Office Open XML WordprocessingML Vorlage (makrofrei).

### EPUB {#EPUB}
```
public static int EPUB
```


EPUB-Format.

### FLAT_OPC {#FLAT-OPC}
```
public static int FLAT_OPC
```


Office Open XML WordprocessingML, gespeichert in einer flachen XML-Datei anstelle eines ZIP-Pakets.

### FLAT_OPC_MACRO_ENABLED {#FLAT-OPC-MACRO-ENABLED}
```
public static int FLAT_OPC_MACRO_ENABLED
```


Office Open XML WordprocessingML Makroaktiviertes Dokument, gespeichert in einer flachen XML-Datei anstelle eines ZIP-Pakets.

### FLAT_OPC_TEMPLATE {#FLAT-OPC-TEMPLATE}
```
public static int FLAT_OPC_TEMPLATE
```


Office Open XML WordprocessingML Vorlage (makrofrei) gespeichert in einer flachen XML-Datei anstelle eines ZIP-Pakets.

### FLAT_OPC_TEMPLATE_MACRO_ENABLED {#FLAT-OPC-TEMPLATE-MACRO-ENABLED}
```
public static int FLAT_OPC_TEMPLATE_MACRO_ENABLED
```


Office Open XML WordprocessingML-Makroaktivierte Vorlage gespeichert in einer flachen XML-Datei anstelle eines ZIP-Pakets.

### HTML {#HTML}
```
public static int HTML
```


HTML-Format.

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


Markdown-Textdokument.

### MHTML {#MHTML}
```
public static int MHTML
```


MHTML (Web-Archiv) Format.

### MOBI {#MOBI}
```
public static int MOBI
```


MOBI-Format. Verwendet vom MobiPocket‑Reader und von Amazon Kindle‑Lesegeräten.

### MS_WORKS {#MS-WORKS}
```
public static int MS_WORKS
```


Microsoft Works 8 Dokument.

### ODT {#ODT}
```
public static int ODT
```


ODF-Textdokument.

### OTT {#OTT}
```
public static int OTT
```


ODF-Textdokumentvorlage.

### PDF {#PDF}
```
public static int PDF
```


PDF-Dokument.

### RTF {#RTF}
```
public static int RTF
```


RTF-Format.

### TEXT {#TEXT}
```
public static int TEXT
```


Klartext.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Unbekanntes Format, kann nicht von Aspose.Words geladen werden.

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


Microsoft Word 2003 WordprocessingML-Format.

### XML {#XML}
```
public static int XML
```


XML-Dokument.

### length {#length}
```
public static int length
```


### fromName(String loadFormatName) {#fromName-java.lang.String}
```
public static int fromName(String loadFormatName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| loadFormatName | java.lang.String |  |

**Returns:**
int
### getName(int loadFormat) {#getName-int}
```
public static String getName(int loadFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| loadFormat | int |  |

**Returns:**
java.lang.String
