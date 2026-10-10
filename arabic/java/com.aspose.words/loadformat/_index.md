---
title: "LoadFormat"
linktitle: "LoadFormat"
second_title: "Aspose.Words لـ Java"
description: "يشير إلى تنسيق المستند الذي سيتم تحميله في Java."
type: docs
weight: 434
url: /ar/java/com.aspose.words/loadformat/
---

**Inheritance:**
java.lang.Object
```
public class LoadFormat
```

يشير إلى تنسيق المستند الذي سيتم تحميله.

 **Examples:** 

يوضح كيفية إدراج محتويات HTML من صفحة ويب إلى مستند جديد.

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

يوضح كيفية استخدام طرق FileFormatUtil لاكتشاف تنسيق المستند.

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

يوضح كيفية تحديد URI أساسي عند فتح مستند html.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [AUTO](#AUTO) | يُوجه Aspose.Words للتعرف على التنسيق تلقائيًا. |
| [AZW_3](#AZW-3) | تنسيق AZW3. |
| [CHM](#CHM) | تنسيق CHM (Compiled HTML Help). |
| [DOC](#DOC) | مستند Microsoft Word 95 أو Word 97 - 2003. |
| [DOCM](#DOCM) | مستند Office Open XML WordprocessingML مع تمكين الماكرو. |
| [DOCX](#DOCX) | مستند Office Open XML WordprocessingML (بدون ماكرو). |
| [DOC_PRE_WORD_60](#DOC-PRE-WORD-60) | المستند بتنسيق ما قبل Word 95. |
| [DOT](#DOT) | قالب Microsoft Word 95 أو Word 97 - 2003. |
| [DOTM](#DOTM) | قالب Office Open XML WordprocessingML مع تمكين الماكرو. |
| [DOTX](#DOTX) | قالب Office Open XML WordprocessingML (بدون ماكرو). |
| [EPUB](#EPUB) | تنسيق EPUB. |
| [FLAT_OPC](#FLAT-OPC) | Office Open XML WordprocessingML مخزن في ملف XML مسطح بدلاً من حزمة ZIP. |
| [FLAT_OPC_MACRO_ENABLED](#FLAT-OPC-MACRO-ENABLED) | مستند Office Open XML WordprocessingML Macro-Enabled Document مخزن في ملف XML مسطح بدلاً من حزمة ZIP. |
| [FLAT_OPC_TEMPLATE](#FLAT-OPC-TEMPLATE) | قالب Office Open XML WordprocessingML (بدون ماكرو) مخزن في ملف XML مسطح بدلاً من حزمة ZIP. |
| [FLAT_OPC_TEMPLATE_MACRO_ENABLED](#FLAT-OPC-TEMPLATE-MACRO-ENABLED) | قالب Office Open XML WordprocessingML Macro-Enabled مخزن في ملف XML مسطح بدلاً من حزمة ZIP. |
| [HTML](#HTML) | تنسيق HTML. |
| [MARKDOWN](#MARKDOWN) | مستند نصي Markdown. |
| [MHTML](#MHTML) | تنسيق MHTML (أرشيف ويب). |
| [MOBI](#MOBI) | تنسيق MOBI. |
| [MS_WORKS](#MS-WORKS) | مستند Microsoft Works 8. |
| [ODT](#ODT) | مستند نصي ODF. |
| [OTT](#OTT) | قالب مستند نصي ODF. |
| [PDF](#PDF) | مستند PDF. |
| [RTF](#RTF) | تنسيق RTF. |
| [TEXT](#TEXT) | نص عادي. |
| [UNKNOWN](#UNKNOWN) | تنسيق غير معروف، لا يمكن تحميله بواسطة Aspose.Words. |
| [WORD_ML](#WORD-ML) | تنسيق Microsoft Word 2003 WordprocessingML. |
| [XML](#XML) | مستند XML. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String loadFormatName)](#fromName-java.lang.String) |  |
| [getName(int loadFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int loadFormat)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


يُوجه Aspose.Words للتعرف على التنسيق تلقائيًا.

### AZW_3 {#AZW-3}
```
public static int AZW_3
```


تنسيق AZW3. يُستخدم بواسطة قارئات Amazon Kindle.

### CHM {#CHM}
```
public static int CHM
```


تنسيق CHM (Compiled HTML Help).

### DOC {#DOC}
```
public static int DOC
```


مستند Microsoft Word 95 أو Word 97 - 2003.

### DOCM {#DOCM}
```
public static int DOCM
```


مستند Office Open XML WordprocessingML مع تمكين الماكرو.

### DOCX {#DOCX}
```
public static int DOCX
```


مستند Office Open XML WordprocessingML (بدون ماكرو).

### DOC_PRE_WORD_60 {#DOC-PRE-WORD-60}
```
public static int DOC_PRE_WORD_60
```


المستند بتنسيق ما قبل Word 95. لا يدعم Aspose.Words حالياً تحميل مثل هذه المستندات.

### DOT {#DOT}
```
public static int DOT
```


قالب Microsoft Word 95 أو Word 97 - 2003.

### DOTM {#DOTM}
```
public static int DOTM
```


قالب Office Open XML WordprocessingML مع تمكين الماكرو.

### DOTX {#DOTX}
```
public static int DOTX
```


قالب Office Open XML WordprocessingML (بدون ماكرو).

### EPUB {#EPUB}
```
public static int EPUB
```


تنسيق EPUB.

### FLAT_OPC {#FLAT-OPC}
```
public static int FLAT_OPC
```


Office Open XML WordprocessingML مخزن في ملف XML مسطح بدلاً من حزمة ZIP.

### FLAT_OPC_MACRO_ENABLED {#FLAT-OPC-MACRO-ENABLED}
```
public static int FLAT_OPC_MACRO_ENABLED
```


مستند Office Open XML WordprocessingML Macro-Enabled Document مخزن في ملف XML مسطح بدلاً من حزمة ZIP.

### FLAT_OPC_TEMPLATE {#FLAT-OPC-TEMPLATE}
```
public static int FLAT_OPC_TEMPLATE
```


قالب Office Open XML WordprocessingML (بدون ماكرو) مخزن في ملف XML مسطح بدلاً من حزمة ZIP.

### FLAT_OPC_TEMPLATE_MACRO_ENABLED {#FLAT-OPC-TEMPLATE-MACRO-ENABLED}
```
public static int FLAT_OPC_TEMPLATE_MACRO_ENABLED
```


قالب Office Open XML WordprocessingML Macro-Enabled مخزن في ملف XML مسطح بدلاً من حزمة ZIP.

### HTML {#HTML}
```
public static int HTML
```


تنسيق HTML.

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


مستند نصي Markdown.

### MHTML {#MHTML}
```
public static int MHTML
```


تنسيق MHTML (أرشيف ويب).

### MOBI {#MOBI}
```
public static int MOBI
```


تنسيق MOBI. يُستخدم بواسطة قارئ MobiPocket وقارئات Amazon Kindle.

### MS_WORKS {#MS-WORKS}
```
public static int MS_WORKS
```


مستند Microsoft Works 8.

### ODT {#ODT}
```
public static int ODT
```


مستند نصي ODF.

### OTT {#OTT}
```
public static int OTT
```


قالب مستند نصي ODF.

### PDF {#PDF}
```
public static int PDF
```


مستند PDF.

### RTF {#RTF}
```
public static int RTF
```


تنسيق RTF.

### TEXT {#TEXT}
```
public static int TEXT
```


نص عادي.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


تنسيق غير معروف، لا يمكن تحميله بواسطة Aspose.Words.

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


تنسيق Microsoft Word 2003 WordprocessingML.

### XML {#XML}
```
public static int XML
```


مستند XML.

### length {#length}
```
public static int length
```


### fromName(String loadFormatName) {#fromName-java.lang.String}
```
public static int fromName(String loadFormatName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| loadFormatName | java.lang.String |  |

**Returns:**
int
### getName(int loadFormat) {#getName-int}
```
public static String getName(int loadFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| loadFormat | int |  |

**Returns:**
java.lang.String
