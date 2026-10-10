---
title: "LoadFormat"
linktitle: "LoadFormat"
second_title: "Aspose.Words Java için"
description: "Java'da yüklenecek belgenin formatını gösterir."
type: docs
weight: 434
url: /tr/java/com.aspose.words/loadformat/
---

**Inheritance:**
java.lang.Object
```
public class LoadFormat
```

Yüklenecek belgenin formatını gösterir.

 **Examples:** 

Bir web sayfasının HTML içeriğini yeni bir belgeye nasıl ekleyeceğinizi gösterir.

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

Bir belgenin formatını tespit etmek için FileFormatUtil yöntemlerinin nasıl kullanılacağını gösterir.

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

HTML belgesi açarken temel bir URI nasıl belirtileceğini gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [AUTO](#AUTO) | Aspose.Words'ı formatı otomatik olarak tanıması için yönlendirir. |
| [AZW_3](#AZW-3) | AZW3 formatı. |
| [CHM](#CHM) | CHM (Derlenmiş HTML Yardım) formatı. |
| [DOC](#DOC) | Microsoft Word 95 veya Word 97 - 2003 Belgesi. |
| [DOCM](#DOCM) | Office Open XML WordprocessingML Makro Etkin Belgesi. |
| [DOCX](#DOCX) | Office Open XML WordprocessingML Belgesi (makrosuz). |
| [DOC_PRE_WORD_60](#DOC-PRE-WORD-60) | Belge, Word 95 öncesi formatındadır. |
| [DOT](#DOT) | Microsoft Word 95 veya Word 97 - 2003 Şablonu. |
| [DOTM](#DOTM) | Office Open XML WordprocessingML Makro Etkin Şablonu. |
| [DOTX](#DOTX) | Office Open XML WordprocessingML Şablonu (makrosuz). |
| [EPUB](#EPUB) | EPUB formatı. |
| [FLAT_OPC](#FLAT-OPC) | ZIP paketi yerine düz bir XML dosyasında depolanan Office Open XML WordprocessingML. |
| [FLAT_OPC_MACRO_ENABLED](#FLAT-OPC-MACRO-ENABLED) | ZIP paketi yerine düz bir XML dosyasında depolanan Office Open XML WordprocessingML Makro Etkin Belge. |
| [FLAT_OPC_TEMPLATE](#FLAT-OPC-TEMPLATE) | ZIP paketi yerine düz bir XML dosyasında depolanan Office Open XML WordprocessingML Şablonu (makrosuz). |
| [FLAT_OPC_TEMPLATE_MACRO_ENABLED](#FLAT-OPC-TEMPLATE-MACRO-ENABLED) | ZIP paketi yerine düz bir XML dosyasında depolanan Office Open XML WordprocessingML Makro Etkin Şablon. |
| [HTML](#HTML) | HTML biçimi. |
| [MARKDOWN](#MARKDOWN) | Markdown metin belgesi. |
| [MHTML](#MHTML) | MHTML (Web arşivi) biçimi. |
| [MOBI](#MOBI) | MOBI biçimi. |
| [MS_WORKS](#MS-WORKS) | Microsoft Works 8 Belgesi. |
| [ODT](#ODT) | ODF Metin Belgesi. |
| [OTT](#OTT) | ODF Metin Belgesi Şablonu. |
| [PDF](#PDF) | Pdf belgesi. |
| [RTF](#RTF) | RTF biçimi. |
| [TEXT](#TEXT) | Düz Metin. |
| [UNKNOWN](#UNKNOWN) | Tanımlanamayan biçim, Aspose.Words tarafından yüklenemiyor. |
| [WORD_ML](#WORD-ML) | Microsoft Word 2003 WordprocessingML biçimi. |
| [XML](#XML) | XML belgesi. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String loadFormatName)](#fromName-java.lang.String) |  |
| [getName(int loadFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int loadFormat)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Aspose.Words'ı formatı otomatik olarak tanıması için yönlendirir.

### AZW_3 {#AZW-3}
```
public static int AZW_3
```


AZW3 biçimi. Amazon Kindle okuyucular tarafından kullanılır.

### CHM {#CHM}
```
public static int CHM
```


CHM (Derlenmiş HTML Yardım) formatı.

### DOC {#DOC}
```
public static int DOC
```


Microsoft Word 95 veya Word 97 - 2003 Belgesi.

### DOCM {#DOCM}
```
public static int DOCM
```


Office Open XML WordprocessingML Makro Etkin Belgesi.

### DOCX {#DOCX}
```
public static int DOCX
```


Office Open XML WordprocessingML Belgesi (makrosuz).

### DOC_PRE_WORD_60 {#DOC-PRE-WORD-60}
```
public static int DOC_PRE_WORD_60
```


Belge Word 95 öncesi bir biçimde. Aspose.Words şu anda bu tür belgeleri yüklemeyi desteklemiyor.

### DOT {#DOT}
```
public static int DOT
```


Microsoft Word 95 veya Word 97 - 2003 Şablonu.

### DOTM {#DOTM}
```
public static int DOTM
```


Office Open XML WordprocessingML Makro Etkin Şablonu.

### DOTX {#DOTX}
```
public static int DOTX
```


Office Open XML WordprocessingML Şablonu (makrosuz).

### EPUB {#EPUB}
```
public static int EPUB
```


EPUB formatı.

### FLAT_OPC {#FLAT-OPC}
```
public static int FLAT_OPC
```


ZIP paketi yerine düz bir XML dosyasında depolanan Office Open XML WordprocessingML.

### FLAT_OPC_MACRO_ENABLED {#FLAT-OPC-MACRO-ENABLED}
```
public static int FLAT_OPC_MACRO_ENABLED
```


ZIP paketi yerine düz bir XML dosyasında depolanan Office Open XML WordprocessingML Makro Etkin Belge.

### FLAT_OPC_TEMPLATE {#FLAT-OPC-TEMPLATE}
```
public static int FLAT_OPC_TEMPLATE
```


ZIP paketi yerine düz bir XML dosyasında depolanan Office Open XML WordprocessingML Şablonu (makrosuz).

### FLAT_OPC_TEMPLATE_MACRO_ENABLED {#FLAT-OPC-TEMPLATE-MACRO-ENABLED}
```
public static int FLAT_OPC_TEMPLATE_MACRO_ENABLED
```


ZIP paketi yerine düz bir XML dosyasında depolanan Office Open XML WordprocessingML Makro Etkin Şablon.

### HTML {#HTML}
```
public static int HTML
```


HTML biçimi.

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


Markdown metin belgesi.

### MHTML {#MHTML}
```
public static int MHTML
```


MHTML (Web arşivi) biçimi.

### MOBI {#MOBI}
```
public static int MOBI
```


MOBI biçimi. MobiPocket okuyucu ve Amazon Kindle okuyucular tarafından kullanılır.

### MS_WORKS {#MS-WORKS}
```
public static int MS_WORKS
```


Microsoft Works 8 Belgesi.

### ODT {#ODT}
```
public static int ODT
```


ODF Metin Belgesi.

### OTT {#OTT}
```
public static int OTT
```


ODF Metin Belgesi Şablonu.

### PDF {#PDF}
```
public static int PDF
```


Pdf belgesi.

### RTF {#RTF}
```
public static int RTF
```


RTF biçimi.

### TEXT {#TEXT}
```
public static int TEXT
```


Düz Metin.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Tanımlanamayan biçim, Aspose.Words tarafından yüklenemiyor.

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


Microsoft Word 2003 WordprocessingML biçimi.

### XML {#XML}
```
public static int XML
```


XML belgesi.

### length {#length}
```
public static int length
```


### fromName(String loadFormatName) {#fromName-java.lang.String}
```
public static int fromName(String loadFormatName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| loadFormatName | java.lang.String |  |

**Returns:**
int
### getName(int loadFormat) {#getName-int}
```
public static String getName(int loadFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| loadFormat | int |  |

**Returns:**
java.lang.String
