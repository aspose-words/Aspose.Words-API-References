---
title: "LoadFormat"
linktitle: "LoadFormat"
second_title: "Aspose.Words pour Java"
description: "Indique le format du document qui doit être chargé en Java."
type: docs
weight: 434
url: /fr/java/com.aspose.words/loadformat/
---

**Inheritance:**
java.lang.Object
```
public class LoadFormat
```

Indique le format du document qui doit être chargé.

 **Examples:** 

Montre comment insérer le contenu HTML d'une page Web dans un nouveau document.

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

Montre comment utiliser les méthodes de FileFormatUtil pour détecter le format d'un document.

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

Montre comment spécifier une URI de base lors de l'ouverture d'un document html.

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
## Champs

| Champ | Description |
| --- | --- |
| [AUTO](#AUTO) | Indique à Aspose.Words de reconnaître le format automatiquement. |
| [AZW_3](#AZW-3) | Format AZW3. |
| [CHM](#CHM) | Format CHM (Compiled HTML Help). |
| [DOC](#DOC) | Document Microsoft Word 95 ou Word 97 - 2003. |
| [DOCM](#DOCM) | Document Office Open XML WordprocessingML Macro-Enabled. |
| [DOCX](#DOCX) | Document Office Open XML WordprocessingML (sans macro). |
| [DOC_PRE_WORD_60](#DOC-PRE-WORD-60) | Le document est au format pré-Word 95. |
| [DOT](#DOT) | Modèle Microsoft Word 95 ou Word 97 - 2003. |
| [DOTM](#DOTM) | Modèle Office Open XML WordprocessingML Macro-Enabled. |
| [DOTX](#DOTX) | Modèle Office Open XML WordprocessingML (sans macro). |
| [EPUB](#EPUB) | Format EPUB. |
| [FLAT_OPC](#FLAT-OPC) | Office Open XML WordprocessingML stocké dans un fichier XML plat au lieu d'un package ZIP. |
| [FLAT_OPC_MACRO_ENABLED](#FLAT-OPC-MACRO-ENABLED) | Document Office Open XML WordprocessingML avec macros stocké dans un fichier XML plat au lieu d'un package ZIP. |
| [FLAT_OPC_TEMPLATE](#FLAT-OPC-TEMPLATE) | Modèle Office Open XML WordprocessingML (sans macros) stocké dans un fichier XML plat au lieu d'un package ZIP. |
| [FLAT_OPC_TEMPLATE_MACRO_ENABLED](#FLAT-OPC-TEMPLATE-MACRO-ENABLED) | Modèle Office Open XML WordprocessingML avec macros stocké dans un fichier XML plat au lieu d'un package ZIP. |
| [HTML](#HTML) | Format HTML. |
| [MARKDOWN](#MARKDOWN) | Document texte Markdown. |
| [MHTML](#MHTML) | Format MHTML (archive Web). |
| [MOBI](#MOBI) | Format MOBI. |
| [MS_WORKS](#MS-WORKS) | Document Microsoft Works 8. |
| [ODT](#ODT) | Document texte ODF. |
| [OTT](#OTT) | Modèle de document texte ODF. |
| [PDF](#PDF) | Document PDF. |
| [RTF](#RTF) | Format RTF. |
| [TEXT](#TEXT) | Texte brut. |
| [UNKNOWN](#UNKNOWN) | Format non reconnu, ne peut pas être chargé par Aspose.Words. |
| [WORD_ML](#WORD-ML) | Format Microsoft Word 2003 WordprocessingML. |
| [XML](#XML) | Document XML. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String loadFormatName)](#fromName-java.lang.String) |  |
| [getName(int loadFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int loadFormat)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Indique à Aspose.Words de reconnaître le format automatiquement.

### AZW_3 {#AZW-3}
```
public static int AZW_3
```


Format AZW3. Utilisé par les lecteurs Amazon Kindle.

### CHM {#CHM}
```
public static int CHM
```


Format CHM (Compiled HTML Help).

### DOC {#DOC}
```
public static int DOC
```


Document Microsoft Word 95 ou Word 97 - 2003.

### DOCM {#DOCM}
```
public static int DOCM
```


Document Office Open XML WordprocessingML Macro-Enabled.

### DOCX {#DOCX}
```
public static int DOCX
```


Document Office Open XML WordprocessingML (sans macro).

### DOC_PRE_WORD_60 {#DOC-PRE-WORD-60}
```
public static int DOC_PRE_WORD_60
```


Le document est au format antérieur à Word 95. Aspose.Words ne prend actuellement pas en charge le chargement de tels documents.

### DOT {#DOT}
```
public static int DOT
```


Modèle Microsoft Word 95 ou Word 97 - 2003.

### DOTM {#DOTM}
```
public static int DOTM
```


Modèle Office Open XML WordprocessingML Macro-Enabled.

### DOTX {#DOTX}
```
public static int DOTX
```


Modèle Office Open XML WordprocessingML (sans macro).

### EPUB {#EPUB}
```
public static int EPUB
```


Format EPUB.

### FLAT_OPC {#FLAT-OPC}
```
public static int FLAT_OPC
```


Office Open XML WordprocessingML stocké dans un fichier XML plat au lieu d'un package ZIP.

### FLAT_OPC_MACRO_ENABLED {#FLAT-OPC-MACRO-ENABLED}
```
public static int FLAT_OPC_MACRO_ENABLED
```


Document Office Open XML WordprocessingML avec macros stocké dans un fichier XML plat au lieu d'un package ZIP.

### FLAT_OPC_TEMPLATE {#FLAT-OPC-TEMPLATE}
```
public static int FLAT_OPC_TEMPLATE
```


Modèle Office Open XML WordprocessingML (sans macros) stocké dans un fichier XML plat au lieu d'un package ZIP.

### FLAT_OPC_TEMPLATE_MACRO_ENABLED {#FLAT-OPC-TEMPLATE-MACRO-ENABLED}
```
public static int FLAT_OPC_TEMPLATE_MACRO_ENABLED
```


Modèle Office Open XML WordprocessingML avec macros stocké dans un fichier XML plat au lieu d'un package ZIP.

### HTML {#HTML}
```
public static int HTML
```


Format HTML.

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


Document texte Markdown.

### MHTML {#MHTML}
```
public static int MHTML
```


Format MHTML (archive Web).

### MOBI {#MOBI}
```
public static int MOBI
```


Format MOBI. Utilisé par le lecteur MobiPocket et les lecteurs Amazon Kindle.

### MS_WORKS {#MS-WORKS}
```
public static int MS_WORKS
```


Document Microsoft Works 8.

### ODT {#ODT}
```
public static int ODT
```


Document texte ODF.

### OTT {#OTT}
```
public static int OTT
```


Modèle de document texte ODF.

### PDF {#PDF}
```
public static int PDF
```


Document PDF.

### RTF {#RTF}
```
public static int RTF
```


Format RTF.

### TEXT {#TEXT}
```
public static int TEXT
```


Texte brut.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Format non reconnu, ne peut pas être chargé par Aspose.Words.

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


Format Microsoft Word 2003 WordprocessingML.

### XML {#XML}
```
public static int XML
```


Document XML.

### length {#length}
```
public static int length
```


### fromName(String loadFormatName) {#fromName-java.lang.String}
```
public static int fromName(String loadFormatName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| loadFormatName | java.lang.String |  |

**Returns:**
int
### getName(int loadFormat) {#getName-int}
```
public static String getName(int loadFormat)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| loadFormat | int |  |

**Returns:**
java.lang.String
