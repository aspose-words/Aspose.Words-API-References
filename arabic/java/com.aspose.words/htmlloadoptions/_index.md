---
title: "HtmlLoadOptions"
linktitle: "HtmlLoadOptions"
second_title: "Aspose.Words لـ Java"
description: "يسمح بتحديد خيارات إضافية عند تحميل مستند HTML إلى كائن Document في Java."
type: docs
weight: 382
url: /ar/java/com.aspose.words/htmlloadoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.LoadOptions](../../com.aspose.words/loadoptions/)
```
public class HtmlLoadOptions extends LoadOptions
```

يسمح بتحديد خيارات إضافية عند تحميل مستند HTML إلى كائن [Document](../../com.aspose.words/document/)

لمزيد من المعلومات، زر مقالة الوثائق [ Specify Load Options ][Specify Load Options].

 **Examples:** 

يوضح كيفية دعم التعليقات الشرطية أثناء تحميل مستند HTML.

```

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();

 // If the value is true, then we take VML code into account while parsing the loaded document.
 loadOptions.setSupportVml(supportVml);

 // This document contains a JPEG image within "
```


[Specify Load Options]: https://docs.aspose.com/words/java/specify-load-options/
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [HtmlLoadOptions()](#HtmlLoadOptions) | يُهيئ نسخة جديدة من هذه الفئة بالقيم الافتراضية. |
| [HtmlLoadOptions(String password)](#HtmlLoadOptions-java.lang.String) | اختصار لتهيئة نسخة جديدة من هذه الفئة باستخدام كلمة المرور المحددة لتحميل مستند مشفر. |
| [HtmlLoadOptions(int loadFormat, String password, String baseUri)](#HtmlLoadOptions-int-java.lang.String-java.lang.String) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | يحدد ما إذا كان الكائن المحدد مساويًا في القيمة للكائن الحالي. |
| [getBaseUri()](#getBaseUri) | يحصل على السلسلة التي ستُستخدم لحل عناوين URI النسبية الموجودة في المستند إلى عناوين URI مطلقة عند الحاجة. |
| [getBlockImportMode()](#getBlockImportMode) | يحصل على قيمة تحدد كيفية استيراد خصائص العناصر على مستوى الكتلة. |
| [getConvertMetafilesToPng()](#getConvertMetafilesToPng) | يحصل على ما إذا كان سيتم تحويل ملفات الميتا ( **F:Aspose.FileFormat.Wmf** أو **F:Aspose.FileFormat.Emf**) إلى تنسيق الصورة **F:Aspose.FileFormat.Png**. |
| [getConvertShapeToOfficeMath()](#getConvertShapeToOfficeMath) | يحصل على ما إذا كان سيتم تحويل الأشكال التي تحتوي على EquationXML إلى كائنات Office Math. |
| [getConvertSvgToEmf()](#getConvertSvgToEmf) | يحصل على قيمة تشير إلى ما إذا كان سيتم تحويل صور SVG المحملة إلى تنسيق EMF. |
| [getEncoding()](#getEncoding) | يحصل على الترميز الذي سيُستخدم لتحميل مستند HTML أو TXT أو CHM إذا لم يتم تحديد الترميز داخل المستند. |
| [getFontSettings()](#getFontSettings) | يسمح بتحديد إعدادات خطوط المستند. |
| [getIgnoreNoscriptElements()](#getIgnoreNoscriptElements) | يحصل على قيمة تشير إلى ما إذا كان يجب تجاهل عناصر HTML. |
| [getIgnoreOleData()](#getIgnoreOleData) | يحدد ما إذا كان يجب تجاهل بيانات OLE. |
| [getLanguagePreferences()](#getLanguagePreferences) | يحصل على تفضيلات اللغة التي ستُستخدم عند تحميل المستند. |
| [getLoadFormat()](#getLoadFormat) | يحدد تنسيق المستند الذي سيتم تحميله. |
| [getMswVersion()](#getMswVersion) | يسمح بتحديد أن عملية تحميل المستند يجب أن تتطابق مع إصدار محدد من MS Word. |
| [getPassword()](#getPassword) | يحصل على كلمة المرور لفتح مستند مشفر. |
| [getPreferredControlType()](#getPreferredControlType) | يحصل على النوع المفضل لعقد المستند التي ستمثل العناصر المستوردة  و  . |
| [getPreserveIncludePictureField()](#getPreserveIncludePictureField) | يحصل على ما إذا كان يجب الحفاظ على حقل INCLUDEPICTURE عند قراءة صيغ Microsoft Word. |
| [getProgressCallback()](#getProgressCallback) | يُستدعى أثناء تحميل مستند ويقبل بيانات حول تقدم التحميل. |
| [getRecoveryMode()](#getRecoveryMode) | يحدد كيفية التعامل مع المستند إذا حدثت أخطاء أثناء التحميل. |
| [getResourceLoadingCallback()](#getResourceLoadingCallback) | يسمح بالتحكم في كيفية تحميل الموارد الخارجية (الصور، أوراق الأنماط) عندما يتم استيراد مستند من HTML أو MHTML. |
| [getSupportFontFaceRules()](#getSupportFontFaceRules) | يحصل على قيمة تشير إلى ما إذا كان يجب دعم قواعد @font-face وما إذا كان يجب تحميل الخطوط المعلنة. |
| [getSupportVml()](#getSupportVml) | يحصل على قيمة تشير إلى ما إذا كان يجب دعم صور VML. |
| [getTempFolder()](#getTempFolder) | يسمح باستخدام ملفات مؤقتة عند قراءة المستند. |
| [getUpdateDirtyFields()](#getUpdateDirtyFields) | يحدد ما إذا كان يجب تحديث الحقول باستخدام السمة  dirty . |
| [getUseSystemLcid()](#getUseSystemLcid) | يحصل على ما إذا كان يجب استخدام قيمة LCID المستخرجة من سجل Windows لتحديد هوامش إعداد الصفحة الافتراضية. |
| [getWarningCallback()](#getWarningCallback) | يُستدعى أثناء عملية التحميل، عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق. |
| [getWebRequestTimeout()](#getWebRequestTimeout) | عدد المللي ثانية التي يجب الانتظار قبل انتهاء مهلة طلب الويب. |
| [setBaseUri(String value)](#setBaseUri-java.lang.String) | يضبط السلسلة التي ستُستخدم لحل عناوين URI النسبية الموجودة في المستند إلى عناوين URI مطلقة عند الحاجة. |
| [setBlockImportMode(int value)](#setBlockImportMode-int) | يضبط قيمة تحدد كيفية استيراد خصائص العناصر ذات المستوى الكتلي. |
| [setConvertMetafilesToPng(boolean value)](#setConvertMetafilesToPng-boolean) | يضبط ما إذا كان يجب تحويل صور الميتافايل ( **F:Aspose.FileFormat.Wmf** أو **F:Aspose.FileFormat.Emf**) إلى تنسيق الصورة **F:Aspose.FileFormat.Png**. |
| [setConvertShapeToOfficeMath(boolean value)](#setConvertShapeToOfficeMath-boolean) | يضبط ما إذا كان يجب تحويل الأشكال التي تحتوي على EquationXML إلى كائنات Office Math. |
| [setConvertSvgToEmf(boolean value)](#setConvertSvgToEmf-boolean) | يضبط قيمة تشير إلى ما إذا كان يجب تحويل صور SVG المحملة إلى تنسيق EMF. |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset) | يضبط الترميز الذي سيُستخدم لتحميل مستند HTML أو TXT أو CHM إذا لم يتم تحديد الترميز داخل المستند. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | يسمح بتحديد إعدادات خطوط المستند. |
| [setIgnoreNoscriptElements(boolean value)](#setIgnoreNoscriptElements-boolean) | يضبط قيمة تشير إلى ما إذا كان يجب تجاهل  عناصر HTML. |
| [setIgnoreOleData(boolean value)](#setIgnoreOleData-boolean) | يحدد ما إذا كان يجب تجاهل بيانات OLE. |
| [setLoadFormat(int value)](#setLoadFormat-int) | يحدد تنسيق المستند الذي سيتم تحميله. |
| [setMswVersion(int value)](#setMswVersion-int) | يسمح بتحديد أن عملية تحميل المستند يجب أن تتطابق مع إصدار محدد من MS Word. |
| [setPassword(String value)](#setPassword-java.lang.String) | يضبط كلمة المرور لفتح مستند مشفر. |
| [setPreferredControlType(int value)](#setPreferredControlType-int) | يضبط النوع المفضل لعقد المستند التي ستمثل العناصر المستوردة  و  العناصر. |
| [setPreserveIncludePictureField(boolean value)](#setPreserveIncludePictureField-boolean) | يضبط ما إذا كان يجب الحفاظ على حقل INCLUDEPICTURE عند قراءة صيغ Microsoft Word. |
| [setProgressCallback(IDocumentLoadingCallback value)](#setProgressCallback-com.aspose.words.IDocumentLoadingCallback) | يُستدعى أثناء تحميل مستند ويقبل بيانات حول تقدم التحميل. |
| [setRecoveryMode(int value)](#setRecoveryMode-int) | يحدد كيفية التعامل مع المستند إذا حدثت أخطاء أثناء التحميل. |
| [setResourceLoadingCallback(IResourceLoadingCallback value)](#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback) | يسمح بالتحكم في كيفية تحميل الموارد الخارجية (الصور، أوراق الأنماط) عندما يتم استيراد مستند من HTML أو MHTML. |
| [setSupportFontFaceRules(boolean value)](#setSupportFontFaceRules-boolean) | يضبط قيمة تشير إلى ما إذا كان يجب دعم قواعد @font-face وما إذا كان يجب تحميل الخطوط المعلنة. |
| [setSupportVml(boolean value)](#setSupportVml-boolean) | يضبط قيمة تشير إلى ما إذا كان يجب دعم صور VML. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String) | يسمح باستخدام ملفات مؤقتة عند قراءة المستند. |
| [setUpdateDirtyFields(boolean value)](#setUpdateDirtyFields-boolean) | يحدد ما إذا كان يجب تحديث الحقول باستخدام السمة  dirty . |
| [setUseSystemLcid(boolean value)](#setUseSystemLcid-boolean) | يضبط ما إذا كان يجب استخدام قيمة LCID المستخرجة من سجل Windows لتحديد هوامش إعداد الصفحة الافتراضية. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | يُستدعى أثناء عملية التحميل، عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق. |
| [setWebRequestTimeout(int value)](#setWebRequestTimeout-int) | عدد المللي ثانية التي يجب الانتظار قبل انتهاء مهلة طلب الويب. |
### HtmlLoadOptions() {#HtmlLoadOptions}
```
public HtmlLoadOptions()
```


يُهيئ نسخة جديدة من هذه الفئة بالقيم الافتراضية.

 **Examples:** 

يوضح كيفية دعم التعليقات الشرطية أثناء تحميل مستند HTML.

```

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();

 // If the value is true, then we take VML code into account while parsing the loaded document.
 loadOptions.setSupportVml(supportVml);

 // This document contains a JPEG image within "
```

### HtmlLoadOptions(String password) {#HtmlLoadOptions-java.lang.String}
```
public HtmlLoadOptions(String password)
```


اختصار لتهيئة نسخة جديدة من هذه الفئة باستخدام كلمة المرور المحددة لتحميل مستند مشفر.

 **Examples:** 

يعرض كيفية تشفير مستند Html، ثم فتحه باستخدام كلمة مرور.

```

 // Create and sign an encrypted HTML document from an encrypted .docx.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setComments("Comment");
     signOptions.setSignTime(new Date());
     signOptions.setDecryptionPassword("docPassword");
 }

 String inputFileName = getMyDir() + "Encrypted.docx";
 String outputFileName = getArtifactsDir() + "HtmlLoadOptions.EncryptedHtml.html";
 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);

 // To load and read this document, we will need to pass its decryption
 // password using a HtmlLoadOptions object.
 HtmlLoadOptions loadOptions = new HtmlLoadOptions("docPassword");
 Assert.assertEquals(loadOptions.getPassword(), signOptions.getDecryptionPassword());

 Document doc = new Document(outputFileName, loadOptions);
 Assert.assertEquals(doc.getText().trim(), "Test encrypted document.");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| كلمة مرور | java.lang.String | كلمة المرور لفتح مستند مشفر. يمكن أن تكون  null  أو سلسلة فارغة. |

### HtmlLoadOptions(int loadFormat, String password, String baseUri) {#HtmlLoadOptions-int-java.lang.String-java.lang.String}
```
public HtmlLoadOptions(int loadFormat, String password, String baseUri)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| loadFormat | int |  |
| كلمة مرور | java.lang.String |  |
| baseUri | java.lang.String |  |

### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


يحدد ما إذا كان الكائن المحدد مساويًا في القيمة للكائن الحالي.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getBaseUri() {#getBaseUri}
```
public String getBaseUri()
```


يحصل على السلسلة التي ستُستخدم لحل عناوين URI النسبية الموجودة في المستند إلى عناوين URI مطلقة عند الحاجة. يمكن أن تكون  null  أو سلسلة فارغة. القيمة الافتراضية هي  null .

 **Remarks:** 

يُستخدم هذا الخاصية لحل عناوين URI النسبية إلى مطلقة في الحالات التالية:

1.  عند تحميل مستند HTML من تدفق وتحتوي المستند على صور بعناوين URI نسبية ولا يحتوي على عنوان URI أساسي محدد في عنصر BASE HTML.
2.  عند حفظ مستند إلى PDF وغيرها من الصيغ، لاسترجاع الصور المرتبطة باستخدام عناوين URI نسبية بحيث يمكن حفظ الصور في المستند الناتج.

 **Examples:** 

يوضح كيفية فتح مستند HTML يحتوي على صور من تدفق باستخدام عنوان URI أساسي.

```

 InputStream stream = new FileInputStream(getMyDir() + "Document.html");
 try  {
     // Pass the URI of the base folder while loading it
     // so that any images with relative URIs in the HTML document can be found.
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setBaseUri(getImageDir());

     Document doc = new Document(stream, loadOptions);

     // Verify that the first shape of the document contains a valid image.
     Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

     Assert.assertTrue(shape.isImage());
     Assert.assertNotNull(shape.getImageData().getImageBytes());
     Assert.assertEquals(32.0, ConvertUtil.pointToPixel(shape.getWidth()), 0.01);
     Assert.assertEquals(32.0, ConvertUtil.pointToPixel(shape.getHeight()), 0.01);
 } finally {
     if (stream != null) stream.close();
 }
 
```

**Returns:**
java.lang.String - السلسلة التي ستُستخدم لحل عناوين URI النسبية الموجودة في المستند إلى عناوين URI مطلقة عند الحاجة.
### getBlockImportMode() {#getBlockImportMode}
```
public int getBlockImportMode()
```


يحصل على قيمة تحدد كيفية استيراد خصائص العناصر على مستوى الكتلة. القيمة الافتراضية هي [BlockImportMode.MERGE](../../com.aspose.words/blockimportmode/\#MERGE).

 **Examples:** 

يعرض كيف يتم استيراد خصائص العناصر ذات المستوى الكتلي من المستندات المستندة إلى HTML.

```

 final String html = "\n\n \n \n paragraph 1\n paragraph 2\n\n\n";

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();
 // Set the new mode of import HTML block-level elements.
 loadOptions.setBlockImportMode(blockImportMode);

 Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF_8)), loadOptions);
 doc.save(getArtifactsDir() + "HtmlLoadOptions.BlockImport.docx");
 
```

**Returns:**
int - قيمة تحدد كيفية استيراد خصائص العناصر على مستوى الكتلة. القيمة المرجعة هي واحدة من ثوابت [BlockImportMode](../../com.aspose.words/blockimportmode/).
### getConvertMetafilesToPng() {#getConvertMetafilesToPng}
```
public boolean getConvertMetafilesToPng()
```


يحصل على ما إذا كان سيتم تحويل ملفات الميتا ( **F:Aspose.FileFormat.Wmf** أو **F:Aspose.FileFormat.Emf**) إلى تنسيق الصورة **F:Aspose.FileFormat.Png**.

 **Remarks:** 

الملفات الوصفية ( **F:Aspose.FileFormat.Wmf** أو **F:Aspose.FileFormat.Emf**) هي صيغة صورة غير مضغوطة وأحيانًا تتطلب الكثير من الذاكرة RAM لحفظ ومعالجة المستند. يتيح هذا الخيار تحويل جميع صور الملفات الوصفية إلى **F:Aspose.FileFormat.Png** عند تحميل المستند. يرجى ملاحظة - تحويل الرسومات المتجهة إلى نقطية يقلل من جودة الصور.

 **Examples:** 

يوضح كيفية تحويل WMF/EMF إلى PNG أثناء تحميل المستند.

```

 Document doc = new Document();

 Shape shape = new Shape(doc, ShapeType.IMAGE);
 shape.getImageData().setImage(getImageDir() + "Windows MetaFile.wmf");
 shape.setWidth(100.0);
 shape.setHeight(100.0);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(shape);

 doc.save(getArtifactsDir() + "Image.CreateImageDirectly.docx");

 shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 TestUtil.verifyImageInShape(1600, 1600, ImageType.WMF, shape);

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setConvertMetafilesToPng(true);

 doc = new Document(getArtifactsDir() + "Image.CreateImageDirectly.docx", loadOptions);
 shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 TestUtil.verifyImageInShape(1600, 1600, ImageType.PNG, shape);
 
```

**Returns:**
boolean - ما إذا كان سيتم تحويل صور الملفات الوصفية ( **F:Aspose.FileFormat.Wmf** أو **F:Aspose.FileFormat.Emf**) إلى صيغة الصورة **F:Aspose.FileFormat.Png**.
### getConvertShapeToOfficeMath() {#getConvertShapeToOfficeMath}
```
public boolean getConvertShapeToOfficeMath()
```


يحصل على ما إذا كان سيتم تحويل الأشكال التي تحتوي على EquationXML إلى كائنات Office Math.

 **Examples:** 

يوضح كيفية تحويل أشكال EquationXML إلى كائنات Office Math.

```

 LoadOptions loadOptions = new LoadOptions();

 // Use this flag to specify whether to convert the shapes with EquationXML attributes
 // to Office Math objects and then load the document.
 loadOptions.setConvertShapeToOfficeMath(isConvertShapeToOfficeMath);

 Document doc = new Document(getMyDir() + "Math shapes.docx", loadOptions);

 if (isConvertShapeToOfficeMath) {
     Assert.assertEquals(16, doc.getChildNodes(NodeType.SHAPE, true).getCount());
     Assert.assertEquals(34, doc.getChildNodes(NodeType.OFFICE_MATH, true).getCount());
 } else {
     Assert.assertEquals(24, doc.getChildNodes(NodeType.SHAPE, true).getCount());
     Assert.assertEquals(0, doc.getChildNodes(NodeType.OFFICE_MATH, true).getCount());
 }
 
```

**Returns:**
boolean - ما إذا كان سيتم تحويل الأشكال التي تحتوي على EquationXML إلى كائنات Office Math.
### getConvertSvgToEmf() {#getConvertSvgToEmf}
```
public boolean getConvertSvgToEmf()
```


يحصل على قيمة تشير إلى ما إذا كان سيتم تحويل صور SVG المحملة إلى صيغة EMF. القيمة الافتراضية هي  false  وإذا كان ممكنًا، تُحفظ صور SVG المحملة كما هي دون تحويل.

 **Remarks:** 

الإصدارات الأحدث من MS Word تدعم صور SVG أصلاً. إذا كان إصدار MS Word المحدد في خيارات التحميل يدعم SVG، سيقوم Aspose.Words بحفظ صور SVG كما هي دون تحويل. إذا لم يكن SVG مدعومًا، سيتم تحويل صور SVG المحملة إلى صيغة EMF.

إذا، مع ذلك، تم ضبط هذا الخيار على  true , سيقوم Aspose.Words بتحويل صور SVG المحملة إلى EMF حتى إذا كانت صور SVG مدعومة من قبل الإصدار المحدد من MS Word.

 **Examples:** 

يوضح كيفية تحويل كائنات SVG إلى صيغة مختلفة عند حفظ مستندات HTML.

```

 String html =
     "\n                    \n                        Hello world!\n                    \n                ";

 // Use 'ConvertSvgToEmf' to turn back the legacy behavior
 // where all SVG images loaded from an HTML document were converted to EMF.
 // Now SVG images are loaded without conversion
 // if the MS Word version specified in load options supports SVG images natively.
 HtmlLoadOptions loadOptions = new HtmlLoadOptions(); { loadOptions.setConvertSvgToEmf(true); }

 Document doc = new Document(new ByteArrayInputStream(html.getBytes()));

 // This document contains a  element in the form of text.
 // When we save the document to HTML, we can pass a SaveOptions object
 // to determine how the saving operation handles this object.
 // Setting the "MetafileFormat" property to "HtmlMetafileFormat.Png" to convert it to a PNG image.
 // Setting the "MetafileFormat" property to "HtmlMetafileFormat.Svg" preserve it as a SVG object.
 // Setting the "MetafileFormat" property to "HtmlMetafileFormat.EmfOrWmf" to convert it to a metafile.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setMetafileFormat(htmlMetafileFormat);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.MetafileFormat.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.MetafileFormat.html"), StandardCharsets.UTF_8);

 switch (htmlMetafileFormat) {
     case HtmlMetafileFormat.PNG:
         Assert.assertTrue(outDocContents.contains(
                 " " +
                         "" +
                         ""));
         break;
     case HtmlMetafileFormat.SVG:
         Assert.assertTrue(outDocContents.contains(
                 "" +
                         ""));
         break;
     case HtmlMetafileFormat.EMF_OR_WMF:
         Assert.assertTrue(outDocContents.contains(
                 " " +
                         "" +
                         ""));
         break;
 }
 
```

**Returns:**
boolean - قيمة تشير إلى ما إذا كان سيتم تحويل صور SVG المحملة إلى صيغة EMF.
### getEncoding() {#getEncoding}
```
public Charset getEncoding()
```


يحصل على الترميز الذي سيُستخدم لتحميل مستند HTML أو TXT أو CHM إذا لم يتم تحديد الترميز داخل المستند. يمكن أن يكون  null . القيمة الافتراضية هي  null .

 **Remarks:** 

يُستخدم هذا الخاصية فقط عند تحميل مستندات HTML أو TXT أو CHM.

إذا لم يتم تحديد الترميز داخل المستند وكانت هذه الخاصية  null , فستحاول النظام اكتشاف الترميز تلقائيًا.

 **Examples:** 

يوضح كيفية تعيين الترميز الذي سيتم فتح المستند به.

```

 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setEncoding(StandardCharsets.US_ASCII);
 }

 // Load the document while passing the LoadOptions object, then verify the document's contents.
 Document doc = new Document(getMyDir() + "English text.txt", loadOptions);

 Assert.assertTrue(doc.toString(SaveFormat.TEXT).contains("This is a sample text in English."));
 
```

**Returns:**
java.nio.charset.Charset - الترميز الذي سيُستخدم لتحميل مستند HTML أو TXT أو CHM إذا لم يتم تحديد الترميز داخل المستند.
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


يسمح بتحديد إعدادات خطوط المستند.

 **Remarks:** 

عند تحميل بعض الصيغ، قد يحتاج Aspose.Words إلى حل الخطوط. على سبيل المثال، عند تحميل مستندات HTML قد يقوم Aspose.Words بحل الخطوط لتنفيذ fallback للخط.

إذا تم ضبطه على  null , سيتم استخدام إعدادات الخط الثابتة الافتراضية [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance).

القيمة الافتراضية هي  null .

 **Examples:** 

يوضح كيفية تعيين بدائل الخطوط أثناء التحميل.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setFontSettings(new FontSettings());

 // Set a font substitution rule for a LoadOptions object.
 // If the document we are loading uses a font which we do not have,
 // this rule will substitute the unavailable font with one that does exist.
 // In this case, all uses of the "MissingFont" will convert to "Comic Sans MS".
 TableSubstitutionRule substitutionRule = loadOptions.getFontSettings().getSubstitutionSettings().getTableSubstitution();
 substitutionRule.addSubstitutes("MissingFont", "Comic Sans MS");

 Document doc = new Document(getMyDir() + "Missing font.html", loadOptions);

 // At this point such text will still be in "MissingFont".
 // Font substitution will take place when we render the document.
 Assert.assertEquals("MissingFont", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getFont().getName());

 doc.save(getArtifactsDir() + "FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
 
```

يوضح كيفية تطبيق إعدادات استبدال الخطوط أثناء تحميل المستند.

```

 // Create a FontSettings object that will substitute the "Times New Roman" font
 // with the font "Arvo" from our "MyFonts" folder.
 FontSettings fontSettings = new FontSettings();
 fontSettings.setFontsFolder(getFontsDir(), false);
 fontSettings.getSubstitutionSettings().getTableSubstitution().addSubstitutes("Times New Roman", "Arvo");

 // Set that FontSettings object as a property of a newly created LoadOptions object.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setFontSettings(fontSettings);

 // Load the document, then render it as a PDF with the font substitution.
 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.FontSettings.pdf");
 
```

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getIgnoreNoscriptElements() {#getIgnoreNoscriptElements}
```
public boolean getIgnoreNoscriptElements()
```


يحصل على قيمة تشير إلى ما إذا كان يجب تجاهل عناصر  HTML. القيمة الافتراضية هي  false .

 **Remarks:** 

مثل MS Word، لا يدعم Aspose.Words النصوص البرمجية وبشكل افتراضي يقوم بتحميل محتوى عناصر  إلى المستند الناتج. ومع ذلك، تدعم معظم المتصفحات النصوص البرمجية ولا يكون محتوى  مرئياً. ضبط هذه الخاصية على  true  يجبر Aspose.Words على تجاهل جميع عناصر  ويساعد في إنتاج مستندات تبدو أقرب إلى ما يُرى في المتصفحات.

 **Examples:** 

يوضح كيفية تجاهل عناصر  HTML.

```

 final String html = "\r\n\r\n\r\nNOSCRIPT\r\n\r\n\r\n\r\n\r\n Your browser does not support JavaScript!\r\n\r\n";

 HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions();
 htmlLoadOptions.setIgnoreNoscriptElements(ignoreNoscriptElements);

 Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF_8)), htmlLoadOptions);
 doc.save(getArtifactsDir() + "HtmlLoadOptions.IgnoreNoscriptElements.pdf");
 
```

**Returns:**
boolean - قيمة تشير إلى ما إذا كان يجب تجاهل عناصر  HTML.
### getIgnoreOleData() {#getIgnoreOleData}
```
public boolean getIgnoreOleData()
```


يحدد ما إذا كان يجب تجاهل بيانات OLE.

 **Remarks:** 

قد يؤدي تجاهل بيانات OLE إلى تقليل استهلاك الذاكرة وزيادة الأداء دون فقدان البيانات في حالة عدم دعم تنسيق الوجهة لكائنات OLE.

القيمة الافتراضية هي false.

 **Examples:** 

يوضح كيفية تجاهل بيانات OLE أثناء التحميل.

```

 // Ignoring OLE data may reduce memory consumption and increase performance
 // without data lost in a case when destination format does not support OLE objects.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setIgnoreOleData(true);
 Document doc = new Document(getMyDir() + "OLE objects.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.IgnoreOleData.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getLanguagePreferences() {#getLanguagePreferences}
```
public LanguagePreferences getLanguagePreferences()
```


يحصل على تفضيلات اللغة التي ستُستخدم عند تحميل المستند.

 **Examples:** 

يوضح كيفية تطبيق تفضيلات اللغة عند تحميل مستند.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.getLanguagePreferences().addEditingLanguage(EditingLanguage.JAPANESE);

 Document doc = new Document(getMyDir() + "No default editing language.docx", loadOptions);

 int localeIdFarEast = doc.getStyles().getDefaultFont().getLocaleIdFarEast();
 System.out.println(localeIdFarEast == EditingLanguage.JAPANESE
         ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
         : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
 
```

**Returns:**
[LanguagePreferences](../../com.aspose.words/languagepreferences/) - Language preferences that will be used when document is loading.
### getLoadFormat() {#getLoadFormat}
```
public int getLoadFormat()
```


يحدد تنسيق المستند الذي سيتم تحميله. القيمة الافتراضية هي [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO).

 **Remarks:** 

يوصى بتحديد قيمة [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO) والسماح لـ Aspose.Words باكتشاف تنسيق الملف تلقائيًا. إذا كنت تعرف تنسيق المستند الذي ستقوم بتحميله، يمكنك تحديد التنسيق صراحةً وهذا سيقلل قليلاً من وقت التحميل بسبب العبء المرتبط باكتشاف التنسيق تلقائيًا. إذا حددت تنسيق تحميل صريح وكان غير صحيح، سيتم استدعاء الاكتشاف التلقائي وستُجرى محاولة ثانية لتحميل الملف.

 **Examples:** 

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

**Returns:**
int - القيمة المقابلة من نوع  int . القيمة المرجعة هي إحدى ثوابت [LoadFormat](../../com.aspose.words/loadformat/).
### getMswVersion() {#getMswVersion}
```
public int getMswVersion()
```


يسمح بتحديد أن عملية تحميل المستند يجب أن تتطابق مع إصدار MS Word محدد. القيمة الافتراضية هي [MsWordVersion.WORD\_2019](../../com.aspose.words/mswordversion/\#WORD-2019).

 **Remarks:** 

قد تتعامل إصدارات Word المختلفة مع بعض جوانب محتوى المستند وتنسيقه بشكل مختلف قليلاً أثناء عملية التحميل، مما قد يؤدي إلى اختلافات طفيفة في نموذج كائن المستند (Document Object Model).

 **Examples:** 

يوضح كيفية محاكاة إجراء التحميل لإصدار Microsoft Word محدد أثناء تحميل المستند.

```

 // By default, Aspose.Words load documents according to Microsoft Word 2019 specification.
 LoadOptions loadOptions = new LoadOptions();

 Assert.assertEquals(MsWordVersion.WORD_2019, loadOptions.getMswVersion());

 // This document is missing the default paragraph formatting style.
 // This default style will be regenerated when we load the document either with Microsoft Word or Aspose.Words.
 loadOptions.setMswVersion(MsWordVersion.WORD_2007);
 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

 // The style's line spacing will have this value when loaded by Microsoft Word 2007 specification.
 Assert.assertEquals(12.95d, doc.getStyles().getDefaultParagraphFormat().getLineSpacing(), 0.01d);
 
```

**Returns:**
int - القيمة المقابلة من نوع  int . القيمة المرجعة هي إحدى ثوابت [MsWordVersion](../../com.aspose.words/mswordversion/).
### getPassword() {#getPassword}
```
public String getPassword()
```


يحصل على كلمة المرور لفتح مستند مشفر. يمكن أن تكون  null  أو سلسلة فارغة. القيمة الافتراضية هي  null .

 **Remarks:** 

تحتاج إلى معرفة كلمة المرور لفتح مستند مشفر. إذا لم يكن المستند مشفرًا، اضبطه على  null  أو سلسلة فارغة.

 **Examples:** 

يوضح كيفية توقيع ملف مستند مشفر.

```

 // Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a comment, date, and decryption password which will be applied with our new digital signature.
 SignOptions signOptions = new SignOptions();
 {
     signOptions.setComments("Comment");
     signOptions.setSignTime(new Date());
     signOptions.setDecryptionPassword("docPassword");
 }

 // Set a local system filename for the unsigned input document, and an output filename for its new digitally signed copy.
 String inputFileName = getMyDir() + "Encrypted.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.DecryptionPassword.docx";

 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```

**Returns:**
java.lang.String - كلمة المرور لفتح مستند مشفر.
### getPreferredControlType() {#getPreferredControlType}
```
public int getPreferredControlType()
```


يحصل على النوع المفضل لعقد المستند التي ستمثل العناصر المستوردة  و . القيمة الافتراضية هي [HtmlControlType.FORM\_FIELD](../../com.aspose.words/htmlcontroltype/\#FORM-FIELD). ملاحظات: يرجى ملاحظة أن ضبط هذه الخاصية لا يضمن أن جميع العناصر المستوردة ستكون من النوع المحدد. إذا لم يكن عنصر HTML قابلًا للتمثيل بعقد المستند من النوع المفضل، سيستخدم Aspose.Words نوعًا متوافقًا من [HtmlControlType](../../com.aspose.words/htmlcontroltype/) لذلك العنصر. أمثلة: يوضح كيفية تعيين النوع المفضل لعقد المستند التي ستمثل العناصر المستوردة  و .   final String html = "\\r\\n\\r\\n\\r\\n" + "item1\\r\\n\\r\\n\\r\\n\\r\\n"; HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions(); htmlLoadOptions.setPreferredControlType(HtmlControlType.STRUCTURED\_DOCUMENT\_TAG); Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF\_8)), htmlLoadOptions); NodeCollection nodes = doc.getChildNodes(NodeType.STRUCTURED\_DOCUMENT\_TAG, true); StructuredDocumentTag tag = (StructuredDocumentTag) nodes.get(0);

**Returns:**
int - النوع المفضل لعقد المستند التي ستمثل العناصر المستوردة  و . القيمة المرجعة هي إحدى ثوابت [HtmlControlType](../../com.aspose.words/htmlcontroltype/).
### getPreserveIncludePictureField() {#getPreserveIncludePictureField}
```
public boolean getPreserveIncludePictureField()
```


يُحصل على ما إذا كان يجب الحفاظ على حقل INCLUDEPICTURE عند قراءة صيغ Microsoft Word. القيمة الافتراضية هي false.

 **Remarks:** 

بشكل افتراضي، يتم تحويل حقل INCLUDEPICTURE إلى كائن شكل. يمكنك تجاوز ذلك إذا كنت بحاجة إلى الحفاظ على الحقل، على سبيل المثال، إذا رغبت في تحديثه برمجياً. لاحظ مع ذلك أن هذا النهج غير شائع في **Aspose.Words**. استخدمه على مسؤوليتك الخاصة.

أحد حالات الاستخدام الممكنة قد يكون استخدام MERGEFIELD كحقل فرعي لتغيير مسار مصدر الصورة ديناميكياً. في هذه الحالة تحتاج إلى الحفاظ على INCLUDEPICTURE في النموذج.

 **Examples:** 

يوضح كيفية الحفاظ على حقول INCLUDEPICTURE أو تجاهلها عند تحميل مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldIncludePicture includePicture = (FieldIncludePicture) builder.insertField(FieldType.FIELD_INCLUDE_PICTURE, true);
 includePicture.setSourceFullName(getImageDir() + "Transparent background logo.png");
 includePicture.update(true);

 try (ByteArrayOutputStream docStream = new ByteArrayOutputStream()) {
     doc.save(docStream, new OoxmlSaveOptions(SaveFormat.DOCX));

     // We can set a flag in a LoadOptions object to decide whether to convert all INCLUDEPICTURE fields
     // into image shapes when loading a document that contains them.
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setPreserveIncludePictureField(preserveIncludePictureField);
     }

     doc = new Document(new ByteArrayInputStream(docStream.toByteArray()), loadOptions);
     FieldCollection fieldCollection = doc.getRange().getFields();

     if (preserveIncludePictureField) {
         Assert.assertTrue(IterableUtils.matchesAny(fieldCollection, f -> f.getType() == FieldType.FIELD_INCLUDE_PICTURE));

         doc.updateFields();
         doc.save(getArtifactsDir() + "Field.PreserveIncludePicture.docx");
     } else {
         Assert.assertFalse(IterableUtils.matchesAny(fieldCollection, f -> f.getType() == FieldType.FIELD_INCLUDE_PICTURE));
     }
 }
 
```

**Returns:**
منطقي - ما إذا كان يجب الحفاظ على حقل INCLUDEPICTURE عند قراءة صيغ Microsoft Word.
### getProgressCallback() {#getProgressCallback}
```
public IDocumentLoadingCallback getProgressCallback()
```


يُستدعى أثناء تحميل مستند ويقبل بيانات حول تقدم التحميل.

 **Remarks:** 

[LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX), [LoadFormat.FLAT\_OPC](../../com.aspose.words/loadformat/\#FLAT-OPC), [LoadFormat.DOCM](../../com.aspose.words/loadformat/\#DOCM), [LoadFormat.DOTM](../../com.aspose.words/loadformat/\#DOTM), [LoadFormat.DOTX](../../com.aspose.words/loadformat/\#DOTX), [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN), [LoadFormat.RTF](../../com.aspose.words/loadformat/\#RTF), [LoadFormat.WORD\_ML](../../com.aspose.words/loadformat/\#WORD-ML), [LoadFormat.DOC](../../com.aspose.words/loadformat/\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat/\#DOT), [LoadFormat.ODT](../../com.aspose.words/loadformat/\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat/\#OTT) formats supported.

 **Examples:** 

يوضح كيفية إبلاغ المستخدم إذا تجاوز تحميل المستند الوقت المتوقع للتحميل.

```

 public void progressCallback() throws Exception
 {
     LoadingProgressCallback progressCallback = new LoadingProgressCallback();

     LoadOptions loadOptions = new LoadOptions(); { loadOptions.setProgressCallback(progressCallback); }

     try
     {
         new Document(getMyDir() + "Big document.docx", loadOptions);
     }
     catch (IllegalStateException exception)
     {
         System.out.println(exception.getMessage());
         // Handle loading duration issue.
     }
 }

 /// 
 /// Cancel a document loading after the "MaxDuration" seconds.
 /// 
 public static class LoadingProgressCallback implements IDocumentLoadingCallback
 {
     /// 
     /// Ctr.
     /// 
     public LoadingProgressCallback()
     {
         mLoadingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document loading.
     /// 
     /// Loading arguments.
     public void notify(DocumentLoadingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mLoadingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document loading is started.
     /// 
     private Date mLoadingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.5;
 }
 
```

**Returns:**
[IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/) - The corresponding [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/) value.
### getRecoveryMode() {#getRecoveryMode}
```
public int getRecoveryMode()
```


يحدد كيفية معالجة المستند إذا حدثت أخطاء أثناء التحميل. استخدم هذه الخاصية لتحديد ما إذا كان النظام يجب أن يحاول استعادة المستند أو يتبع سلوكًا معرفًا آخر. القيمة الافتراضية هي [DocumentRecoveryMode.TRY\_RECOVER](../../com.aspose.words/documentrecoverymode/\#TRY-RECOVER).

 **Examples:** 

يوضح كيفية محاولة استعادة مستند إذا حدثت أخطاء أثناء التحميل.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setRecoveryMode(DocumentRecoveryMode.TRY_RECOVER);

 Document doc = new Document(getMyDir() + "Corrupted footnotes.docx", loadOptions);
 
```

**Returns:**
عدد صحيح - القيمة المقابلة من نوع int. القيمة المرجعة هي واحدة من ثوابت [DocumentRecoveryMode](../../com.aspose.words/documentrecoverymode/).
### getResourceLoadingCallback() {#getResourceLoadingCallback}
```
public IResourceLoadingCallback getResourceLoadingCallback()
```


يسمح بالتحكم في كيفية تحميل الموارد الخارجية (الصور، أوراق الأنماط) عندما يتم استيراد مستند من HTML أو MHTML.

 **Examples:** 

يوضح كيفية معالجة الموارد الخارجية عند تحميل مستندات Html.

```

 public void loadOptionsCallback() throws Exception {
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setResourceLoadingCallback(new HtmlLinkedResourceLoadingCallback());

     // When we load the document, our callback will handle linked resources such as CSS stylesheets and images.
     Document doc = new Document(getMyDir() + "Images.html", loadOptions);
     doc.save(getArtifactsDir() + "LoadOptions.LoadOptionsCallback.pdf");
 }

 /// 
 /// Prints the filenames of all external stylesheets and substitutes all images of a loaded html document.
 /// 
 private static class HtmlLinkedResourceLoadingCallback implements IResourceLoadingCallback {
     public int resourceLoading(ResourceLoadingArgs args) throws IOException {
         switch (args.getResourceType()) {
             case ResourceType.CSS_STYLE_SHEET:
                 System.out.println(MessageFormat.format("External CSS Stylesheet found upon loading: {0}", args.getOriginalUri()));
                 return ResourceLoadingAction.DEFAULT;
             case ResourceType.IMAGE:
                 System.out.println(MessageFormat.format("External Image found upon loading: {0}", args.getOriginalUri()));

                 final String newImageFilename = "Logo.jpg";
                 System.out.println(MessageFormat.format("\tImage will be substituted with: {0}", newImageFilename));

                 byte[] imageBytes = FileUtils.readFileToByteArray(new File(getImageDir() + newImageFilename));
                 args.setData(imageBytes);

                 return ResourceLoadingAction.USER_PROVIDED;
         }

         return ResourceLoadingAction.DEFAULT;
     }
 }
 
```

**Returns:**
[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) - The corresponding [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) value.
### getSupportFontFaceRules() {#getSupportFontFaceRules}
```
public boolean getSupportFontFaceRules()
```


يُحصل على قيمة تشير إلى ما إذا كان يجب دعم قواعد @font-face وما إذا كان يجب تحميل الخطوط المعلنة. القيمة الافتراضية هي false.

 **Remarks:** 

إذا تم تمكين هذا الخيار، يتم تحميل الخطوط المعلنة في قواعد @font-face وتضمينها في تعريفات الخطوط للمستند الناتج (انظر [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/#getFontInfos)). يجعل ذلك الخطوط المحملة متاحة للعرض ولكن لا يفعّل تلقائيًا تضمين الخطوط عند الحفظ. من أجل حفظ المستند مع الخطوط المحملة، يجب تعيين خاصية [FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/#getEmbedTrueTypeFonts) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/#setEmbedTrueTypeFonts-boolean) في مجموعة [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/#getFontInfos) إلى true.

تنسيقات الخطوط المدعومة هي TTF و EOT و WOFF.

**Returns:**
منطقي - قيمة تشير إلى ما إذا كان يجب دعم قواعد @font-face وما إذا كان يجب تحميل الخطوط المعلنة.
### getSupportVml() {#getSupportVml}
```
public boolean getSupportVml()
```


يحصل على قيمة تشير إلى ما إذا كان يجب دعم صور VML.

 **Examples:** 

يوضح كيفية دعم التعليقات الشرطية أثناء تحميل مستند HTML.

```

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();

 // If the value is true, then we take VML code into account while parsing the loaded document.
 loadOptions.setSupportVml(supportVml);

 // This document contains a JPEG image within "
```

**Returns:**
منطقي - قيمة تشير إلى ما إذا كان يجب دعم صور VML.
### getTempFolder() {#getTempFolder}
```
public String getTempFolder()
```


يسمح باستخدام ملفات مؤقتة عند قراءة المستند. بشكل افتراضي تكون هذه الخاصية null ولا يتم استخدام أي ملفات مؤقتة.

 **Remarks:** 

يجب أن يكون المجلد موجودًا وقابلًا للكتابة، وإلا سيتم رمي استثناء.

**Aspose.Words** تحذف تلقائيًا جميع الملفات المؤقتة عند اكتمال القراءة.

 **Examples:** 

يوضح كيفية تحميل مستند باستخدام ملفات مؤقتة.

```

 // Note that such an approach can reduce memory usage but degrades speed.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setTempFolder("C:\\TempFolder\\");

 // Ensure that the directory exists and load.
 new File(loadOptions.getTempFolder()).mkdir();

 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);
 
```

يوضح كيفية استخدام القرص الصلب بدلاً من الذاكرة عند تحميل مستند.

```

 // When we load a document, various elements are temporarily stored in memory as the save operation occurs.
 // We can use this option to use a temporary folder in the local file system instead,
 // which will reduce our application's memory overhead.
 LoadOptions options = new LoadOptions();
 options.setTempFolder(getArtifactsDir() + "TempFiles");

 // The specified temporary folder must exist in the local file system before the load operation.
 Files.createDirectory(Paths.get(options.getTempFolder()));

 Document doc = new Document(getMyDir() + "Document.docx", options);

 // The folder will persist with no residual contents from the load operation.
 Assert.assertTrue(DocumentHelper.directoryGetFiles(options.getTempFolder(), "*.*").size() == 0);
 
```

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getUpdateDirtyFields() {#getUpdateDirtyFields}
```
public boolean getUpdateDirtyFields()
```


يحدد ما إذا كان يجب تحديث الحقول باستخدام السمة  dirty .

 **Examples:** 

يوضح كيفية استخدام الخاصية الخاصة لتحديث نتيجة الحقل.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Give the document's built-in "Author" property value, and then display it with a field.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 FieldAuthor field = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);

 Assert.assertFalse(field.isDirty());
 Assert.assertEquals("John Doe", field.getResult());

 // Update the property. The field still displays the old value.
 doc.getBuiltInDocumentProperties().setAuthor("John & Jane Doe");

 Assert.assertEquals("John Doe", field.getResult());

 // Since the field's value is out of date, we can mark it as "dirty".
 // This value will stay out of date until we update the field manually with the Field.Update() method.
 field.isDirty(true);

 // If we save without calling an update method,
 // the field will keep displaying the out of date value in the output document.
 doc.save(getArtifactsDir() + "Filed.UpdateDirtyFields.docx");

 // The LoadOptions object has an option to update all fields
 // marked as "dirty" when loading the document.
 LoadOptions options = new LoadOptions();
 options.setUpdateDirtyFields(updateDirtyFields);

 doc = new Document(getArtifactsDir() + "Filed.UpdateDirtyFields.docx", options);

 Assert.assertEquals("John & Jane Doe", doc.getBuiltInDocumentProperties().getAuthor());

 field = (FieldAuthor) doc.getRange().getFields().get(0);

 // Updating dirty fields like this automatically set their "IsDirty" flag to false.
 if (updateDirtyFields) {
     Assert.assertEquals("John & Jane Doe", field.getResult());
     Assert.assertFalse(field.isDirty());
 } else {
     Assert.assertEquals("John Doe", field.getResult());
     Assert.assertTrue(field.isDirty());
 }
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getUseSystemLcid() {#getUseSystemLcid}
```
public boolean getUseSystemLcid()
```


يحصل على ما إذا كان يجب استخدام قيمة LCID المستخرجة من سجل Windows لتحديد هوامش إعداد الصفحة الافتراضية.

 **Remarks:** 

إذا تم تعيينه إلى true، يتم محاكاة سلوك MS Word الذي يأخذ قيمة LCID من سجل Windows.

القيمة الافتراضية هي false.

**Returns:**
منطقي - ما إذا كان يجب استخدام قيمة LCID المستخرجة من سجل Windows لتحديد هوامش إعداد الصفحة الافتراضية.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


يُستدعى أثناء عملية التحميل، عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق.

 **Examples:** 

يوضح كيفية طباعة وتخزين التحذيرات التي تحدث أثناء تحميل المستند.

```

 public void loadOptionsWarningCallback() throws Exception {
     // Create a new LoadOptions object and set its WarningCallback attribute
     // as an instance of our IWarningCallback implementation.
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setWarningCallback(new DocumentLoadingWarningCallback());

     // Our callback will print all warnings that come up during the load operation.
     Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

     ArrayList warnings = ((DocumentLoadingWarningCallback)loadOptions.getWarningCallback()).getWarnings();
     Assert.assertEquals(2, warnings.size());
 }

 /// 
 /// IWarningCallback that prints warnings and their details as they arise during document loading.
 /// 
 private static class DocumentLoadingWarningCallback implements IWarningCallback {
     public void warning(WarningInfo info) {
         System.out.println(MessageFormat.format("Warning: {0}", info.getWarningType()));
         System.out.println(MessageFormat.format("\tSource: {0}", info.getSource()));
         System.out.println(MessageFormat.format("\tDescription: {0}", info.getDescription()));
         mWarnings.add(info);
     }

     public ArrayList getWarnings() {
         return mWarnings;
     }

     private final  ArrayList mWarnings = new ArrayList();
 }
 
```

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### getWebRequestTimeout() {#getWebRequestTimeout}
```
public int getWebRequestTimeout()
```


عدد المللي ثانية للانتظار قبل انتهاء مهلة طلب الويب. القيمة الافتراضية هي 100000 مللي ثانية (100 ثانية).

 **Remarks:** 

عدد المللي ثانية التي تنتظرها **Aspose.Words** للحصول على استجابة عند تحميل الموارد الخارجية (الصور، أوراق الأنماط) المرتبطة في مستندات HTML و MHTML.

**Returns:**
int - القيمة المقابلة  int .
### setBaseUri(String value) {#setBaseUri-java.lang.String}
```
public void setBaseUri(String value)
```


يضبط السلسلة التي ستُستخدم لحل عناوين URI النسبية الموجودة في المستند إلى عناوين URI مطلقة عند الحاجة. يمكن أن تكون null أو سلسلة فارغة. القيمة الافتراضية هي null.

 **Remarks:** 

يُستخدم هذا الخاصية لحل عناوين URI النسبية إلى مطلقة في الحالات التالية:

1.  عند تحميل مستند HTML من تدفق وتحتوي المستند على صور بعناوين URI نسبية ولا يحتوي على عنوان URI أساسي محدد في عنصر BASE HTML.
2.  عند حفظ مستند إلى PDF وغيرها من الصيغ، لاسترجاع الصور المرتبطة باستخدام عناوين URI نسبية بحيث يمكن حفظ الصور في المستند الناتج.

 **Examples:** 

يوضح كيفية فتح مستند HTML يحتوي على صور من تدفق باستخدام عنوان URI أساسي.

```

 InputStream stream = new FileInputStream(getMyDir() + "Document.html");
 try  {
     // Pass the URI of the base folder while loading it
     // so that any images with relative URIs in the HTML document can be found.
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setBaseUri(getImageDir());

     Document doc = new Document(stream, loadOptions);

     // Verify that the first shape of the document contains a valid image.
     Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

     Assert.assertTrue(shape.isImage());
     Assert.assertNotNull(shape.getImageData().getImageBytes());
     Assert.assertEquals(32.0, ConvertUtil.pointToPixel(shape.getWidth()), 0.01);
     Assert.assertEquals(32.0, ConvertUtil.pointToPixel(shape.getHeight()), 0.01);
 } finally {
     if (stream != null) stream.close();
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | السلسلة التي ستُستخدم لحل عناوين URI النسبية الموجودة في المستند إلى عناوين URI مطلقة عند الحاجة. |

### setBlockImportMode(int value) {#setBlockImportMode-int}
```
public void setBlockImportMode(int value)
```


يضبط قيمة تحدد كيفية استيراد خصائص العناصر على مستوى الكتلة. القيمة الافتراضية هي [BlockImportMode.MERGE](../../com.aspose.words/blockimportmode/\#MERGE).

 **Examples:** 

يعرض كيف يتم استيراد خصائص العناصر ذات المستوى الكتلي من المستندات المستندة إلى HTML.

```

 final String html = "\n\n \n \n paragraph 1\n paragraph 2\n\n\n";

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();
 // Set the new mode of import HTML block-level elements.
 loadOptions.setBlockImportMode(blockImportMode);

 Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF_8)), loadOptions);
 doc.save(getArtifactsDir() + "HtmlLoadOptions.BlockImport.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | قيمة تحدد كيفية استيراد خصائص العناصر على مستوى الكتلة. يجب أن تكون القيمة واحدة من ثوابت [BlockImportMode](../../com.aspose.words/blockimportmode/). |

### setConvertMetafilesToPng(boolean value) {#setConvertMetafilesToPng-boolean}
```
public void setConvertMetafilesToPng(boolean value)
```


يضبط ما إذا كان يجب تحويل صور الميتافايل ( **F:Aspose.FileFormat.Wmf** أو **F:Aspose.FileFormat.Emf**) إلى تنسيق الصورة **F:Aspose.FileFormat.Png**.

 **Remarks:** 

الملفات الوصفية ( **F:Aspose.FileFormat.Wmf** أو **F:Aspose.FileFormat.Emf**) هي صيغة صورة غير مضغوطة وأحيانًا تتطلب الكثير من الذاكرة RAM لحفظ ومعالجة المستند. يتيح هذا الخيار تحويل جميع صور الملفات الوصفية إلى **F:Aspose.FileFormat.Png** عند تحميل المستند. يرجى ملاحظة - تحويل الرسومات المتجهة إلى نقطية يقلل من جودة الصور.

 **Examples:** 

يوضح كيفية تحويل WMF/EMF إلى PNG أثناء تحميل المستند.

```

 Document doc = new Document();

 Shape shape = new Shape(doc, ShapeType.IMAGE);
 shape.getImageData().setImage(getImageDir() + "Windows MetaFile.wmf");
 shape.setWidth(100.0);
 shape.setHeight(100.0);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(shape);

 doc.save(getArtifactsDir() + "Image.CreateImageDirectly.docx");

 shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 TestUtil.verifyImageInShape(1600, 1600, ImageType.WMF, shape);

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setConvertMetafilesToPng(true);

 doc = new Document(getArtifactsDir() + "Image.CreateImageDirectly.docx", loadOptions);
 shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 TestUtil.verifyImageInShape(1600, 1600, ImageType.PNG, shape);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | ما إذا كان سيتم تحويل صور ملف التعريف ( **F:Aspose.FileFormat.Wmf** أو **F:Aspose.FileFormat.Emf**) إلى تنسيق الصورة **F:Aspose.FileFormat.Png**. |

### setConvertShapeToOfficeMath(boolean value) {#setConvertShapeToOfficeMath-boolean}
```
public void setConvertShapeToOfficeMath(boolean value)
```


يضبط ما إذا كان يجب تحويل الأشكال التي تحتوي على EquationXML إلى كائنات Office Math.

 **Examples:** 

يوضح كيفية تحويل أشكال EquationXML إلى كائنات Office Math.

```

 LoadOptions loadOptions = new LoadOptions();

 // Use this flag to specify whether to convert the shapes with EquationXML attributes
 // to Office Math objects and then load the document.
 loadOptions.setConvertShapeToOfficeMath(isConvertShapeToOfficeMath);

 Document doc = new Document(getMyDir() + "Math shapes.docx", loadOptions);

 if (isConvertShapeToOfficeMath) {
     Assert.assertEquals(16, doc.getChildNodes(NodeType.SHAPE, true).getCount());
     Assert.assertEquals(34, doc.getChildNodes(NodeType.OFFICE_MATH, true).getCount());
 } else {
     Assert.assertEquals(24, doc.getChildNodes(NodeType.SHAPE, true).getCount());
     Assert.assertEquals(0, doc.getChildNodes(NodeType.OFFICE_MATH, true).getCount());
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | ما إذا كان سيتم تحويل الأشكال التي تحتوي على EquationXML إلى كائنات Office Math. |

### setConvertSvgToEmf(boolean value) {#setConvertSvgToEmf-boolean}
```
public void setConvertSvgToEmf(boolean value)
```


يضبط قيمة تشير إلى ما إذا كان سيتم تحويل صور SVG المحملة إلى تنسيق EMF. القيمة الافتراضية هي false، وإذا كان ذلك ممكنًا، تُحفظ صور SVG المحملة كما هي دون تحويل.

 **Remarks:** 

الإصدارات الأحدث من MS Word تدعم صور SVG أصلاً. إذا كان إصدار MS Word المحدد في خيارات التحميل يدعم SVG، سيقوم Aspose.Words بحفظ صور SVG كما هي دون تحويل. إذا لم يكن SVG مدعومًا، سيتم تحويل صور SVG المحملة إلى صيغة EMF.

إذا، مع ذلك، تم ضبط هذا الخيار على  true , سيقوم Aspose.Words بتحويل صور SVG المحملة إلى EMF حتى إذا كانت صور SVG مدعومة من قبل الإصدار المحدد من MS Word.

 **Examples:** 

يوضح كيفية تحويل كائنات SVG إلى صيغة مختلفة عند حفظ مستندات HTML.

```

 String html =
     "\n                    \n                        Hello world!\n                    \n                ";

 // Use 'ConvertSvgToEmf' to turn back the legacy behavior
 // where all SVG images loaded from an HTML document were converted to EMF.
 // Now SVG images are loaded without conversion
 // if the MS Word version specified in load options supports SVG images natively.
 HtmlLoadOptions loadOptions = new HtmlLoadOptions(); { loadOptions.setConvertSvgToEmf(true); }

 Document doc = new Document(new ByteArrayInputStream(html.getBytes()));

 // This document contains a  element in the form of text.
 // When we save the document to HTML, we can pass a SaveOptions object
 // to determine how the saving operation handles this object.
 // Setting the "MetafileFormat" property to "HtmlMetafileFormat.Png" to convert it to a PNG image.
 // Setting the "MetafileFormat" property to "HtmlMetafileFormat.Svg" preserve it as a SVG object.
 // Setting the "MetafileFormat" property to "HtmlMetafileFormat.EmfOrWmf" to convert it to a metafile.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setMetafileFormat(htmlMetafileFormat);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.MetafileFormat.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.MetafileFormat.html"), StandardCharsets.UTF_8);

 switch (htmlMetafileFormat) {
     case HtmlMetafileFormat.PNG:
         Assert.assertTrue(outDocContents.contains(
                 " " +
                         "" +
                         ""));
         break;
     case HtmlMetafileFormat.SVG:
         Assert.assertTrue(outDocContents.contains(
                 "" +
                         ""));
         break;
     case HtmlMetafileFormat.EMF_OR_WMF:
         Assert.assertTrue(outDocContents.contains(
                 " " +
                         "" +
                         ""));
         break;
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة تشير إلى ما إذا كان سيتم تحويل صور SVG المحملة إلى تنسيق EMF. |

### setEncoding(Charset value) {#setEncoding-java.nio.charset.Charset}
```
public void setEncoding(Charset value)
```


يضبط الترميز الذي سيُستخدم لتحميل مستند HTML أو TXT أو CHM إذا لم يُحدد الترميز داخل المستند. يمكن أن يكون null. القيمة الافتراضية هي null.

 **Remarks:** 

يُستخدم هذا الخاصية فقط عند تحميل مستندات HTML أو TXT أو CHM.

إذا لم يتم تحديد الترميز داخل المستند وكانت هذه الخاصية  null , فستحاول النظام اكتشاف الترميز تلقائيًا.

 **Examples:** 

يوضح كيفية تعيين الترميز الذي سيتم فتح المستند به.

```

 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setEncoding(StandardCharsets.US_ASCII);
 }

 // Load the document while passing the LoadOptions object, then verify the document's contents.
 Document doc = new Document(getMyDir() + "English text.txt", loadOptions);

 Assert.assertTrue(doc.toString(SaveFormat.TEXT).contains("This is a sample text in English."));
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.nio.charset.Charset | الترميز الذي سيُستخدم لتحميل مستند HTML أو TXT أو CHM إذا لم يُحدد الترميز داخل المستند. |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


يسمح بتحديد إعدادات خطوط المستند.

 **Remarks:** 

عند تحميل بعض الصيغ، قد يحتاج Aspose.Words إلى حل الخطوط. على سبيل المثال، عند تحميل مستندات HTML قد يقوم Aspose.Words بحل الخطوط لتنفيذ fallback للخط.

إذا تم ضبطه على  null , سيتم استخدام إعدادات الخط الثابتة الافتراضية [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance).

القيمة الافتراضية هي  null .

 **Examples:** 

يوضح كيفية تعيين بدائل الخطوط أثناء التحميل.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setFontSettings(new FontSettings());

 // Set a font substitution rule for a LoadOptions object.
 // If the document we are loading uses a font which we do not have,
 // this rule will substitute the unavailable font with one that does exist.
 // In this case, all uses of the "MissingFont" will convert to "Comic Sans MS".
 TableSubstitutionRule substitutionRule = loadOptions.getFontSettings().getSubstitutionSettings().getTableSubstitution();
 substitutionRule.addSubstitutes("MissingFont", "Comic Sans MS");

 Document doc = new Document(getMyDir() + "Missing font.html", loadOptions);

 // At this point such text will still be in "MissingFont".
 // Font substitution will take place when we render the document.
 Assert.assertEquals("MissingFont", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getFont().getName());

 doc.save(getArtifactsDir() + "FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
 
```

يوضح كيفية تطبيق إعدادات استبدال الخطوط أثناء تحميل المستند.

```

 // Create a FontSettings object that will substitute the "Times New Roman" font
 // with the font "Arvo" from our "MyFonts" folder.
 FontSettings fontSettings = new FontSettings();
 fontSettings.setFontsFolder(getFontsDir(), false);
 fontSettings.getSubstitutionSettings().getTableSubstitution().addSubstitutes("Times New Roman", "Arvo");

 // Set that FontSettings object as a property of a newly created LoadOptions object.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setFontSettings(fontSettings);

 // Load the document, then render it as a PDF with the font substitution.
 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.FontSettings.pdf");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | القيمة المقابلة لـ [FontSettings](../../com.aspose.words/fontsettings/). |

### setIgnoreNoscriptElements(boolean value) {#setIgnoreNoscriptElements-boolean}
```
public void setIgnoreNoscriptElements(boolean value)
```


يضبط قيمة تشير إلى ما إذا كان سيتم تجاهل عناصر HTML. القيمة الافتراضية هي false.

 **Remarks:** 

مثل MS Word، لا يدعم Aspose.Words النصوص البرمجية وبشكل افتراضي يقوم بتحميل محتوى عناصر  إلى المستند الناتج. ومع ذلك، تدعم معظم المتصفحات النصوص البرمجية ولا يكون محتوى  مرئياً. ضبط هذه الخاصية على  true  يجبر Aspose.Words على تجاهل جميع عناصر  ويساعد في إنتاج مستندات تبدو أقرب إلى ما يُرى في المتصفحات.

 **Examples:** 

يوضح كيفية تجاهل عناصر  HTML.

```

 final String html = "\r\n\r\n\r\nNOSCRIPT\r\n\r\n\r\n\r\n\r\n Your browser does not support JavaScript!\r\n\r\n";

 HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions();
 htmlLoadOptions.setIgnoreNoscriptElements(ignoreNoscriptElements);

 Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF_8)), htmlLoadOptions);
 doc.save(getArtifactsDir() + "HtmlLoadOptions.IgnoreNoscriptElements.pdf");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة تشير إلى ما إذا كان سيتم تجاهل عناصر HTML. |

### setIgnoreOleData(boolean value) {#setIgnoreOleData-boolean}
```
public void setIgnoreOleData(boolean value)
```


يحدد ما إذا كان يجب تجاهل بيانات OLE.

 **Remarks:** 

قد يؤدي تجاهل بيانات OLE إلى تقليل استهلاك الذاكرة وزيادة الأداء دون فقدان البيانات في حالة عدم دعم تنسيق الوجهة لكائنات OLE.

القيمة الافتراضية هي false.

 **Examples:** 

يوضح كيفية تجاهل بيانات OLE أثناء التحميل.

```

 // Ignoring OLE data may reduce memory consumption and increase performance
 // without data lost in a case when destination format does not support OLE objects.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setIgnoreOleData(true);
 Document doc = new Document(getMyDir() + "OLE objects.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.IgnoreOleData.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setLoadFormat(int value) {#setLoadFormat-int}
```
public void setLoadFormat(int value)
```


يحدد تنسيق المستند الذي سيتم تحميله. القيمة الافتراضية هي [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO).

 **Remarks:** 

يوصى بتحديد قيمة [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO) والسماح لـ Aspose.Words باكتشاف تنسيق الملف تلقائيًا. إذا كنت تعرف تنسيق المستند الذي ستقوم بتحميله، يمكنك تحديد التنسيق صراحةً وهذا سيقلل قليلاً من وقت التحميل بسبب العبء المرتبط باكتشاف التنسيق تلقائيًا. إذا حددت تنسيق تحميل صريح وكان غير صحيح، سيتم استدعاء الاكتشاف التلقائي وستُجرى محاولة ثانية لتحميل الملف.

 **Examples:** 

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة الصحيحة (int) المقابلة. يجب أن تكون القيمة واحدة من ثوابت [LoadFormat](../../com.aspose.words/loadformat/). |

### setMswVersion(int value) {#setMswVersion-int}
```
public void setMswVersion(int value)
```


يسمح بتحديد أن عملية تحميل المستند يجب أن تتطابق مع إصدار MS Word محدد. القيمة الافتراضية هي [MsWordVersion.WORD\_2019](../../com.aspose.words/mswordversion/\#WORD-2019).

 **Remarks:** 

قد تتعامل إصدارات Word المختلفة مع بعض جوانب محتوى المستند وتنسيقه بشكل مختلف قليلاً أثناء عملية التحميل، مما قد يؤدي إلى اختلافات طفيفة في نموذج كائن المستند (Document Object Model).

 **Examples:** 

يوضح كيفية محاكاة إجراء التحميل لإصدار Microsoft Word محدد أثناء تحميل المستند.

```

 // By default, Aspose.Words load documents according to Microsoft Word 2019 specification.
 LoadOptions loadOptions = new LoadOptions();

 Assert.assertEquals(MsWordVersion.WORD_2019, loadOptions.getMswVersion());

 // This document is missing the default paragraph formatting style.
 // This default style will be regenerated when we load the document either with Microsoft Word or Aspose.Words.
 loadOptions.setMswVersion(MsWordVersion.WORD_2007);
 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

 // The style's line spacing will have this value when loaded by Microsoft Word 2007 specification.
 Assert.assertEquals(12.95d, doc.getStyles().getDefaultParagraphFormat().getLineSpacing(), 0.01d);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة الصحيحة (int) المقابلة. يجب أن تكون القيمة واحدة من ثوابت [MsWordVersion](../../com.aspose.words/mswordversion/). |

### setPassword(String value) {#setPassword-java.lang.String}
```
public void setPassword(String value)
```


يضبط كلمة المرور لفتح مستند مشفر. يمكن أن تكون null أو سلسلة فارغة. القيمة الافتراضية هي null.

 **Remarks:** 

تحتاج إلى معرفة كلمة المرور لفتح مستند مشفر. إذا لم يكن المستند مشفرًا، اضبطه على  null  أو سلسلة فارغة.

 **Examples:** 

يوضح كيفية توقيع ملف مستند مشفر.

```

 // Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a comment, date, and decryption password which will be applied with our new digital signature.
 SignOptions signOptions = new SignOptions();
 {
     signOptions.setComments("Comment");
     signOptions.setSignTime(new Date());
     signOptions.setDecryptionPassword("docPassword");
 }

 // Set a local system filename for the unsigned input document, and an output filename for its new digitally signed copy.
 String inputFileName = getMyDir() + "Encrypted.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.DecryptionPassword.docx";

 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | كلمة المرور لفتح مستند مشفر. |

### setPreferredControlType(int value) {#setPreferredControlType-int}
```
public void setPreferredControlType(int value)
```


يضبط النوع المفضل لعقد المستند التي ستمثل العناصر المستوردة  و  العناصر. القيمة الافتراضية هي [HtmlControlType.FORM\_FIELD](../../com.aspose.words/htmlcontroltype/\#FORM-FIELD). ملاحظات: يرجى ملاحظة أن ضبط هذه الخاصية لا يضمن أن جميع العناصر المستوردة ستكون من النوع المحدد. إذا لم يكن عنصر HTML قابلًا للتمثيل بعقد المستند من النوع المفضل، سيستخدم Aspose.Words نوعًا متوافقًا من [HtmlControlType](../../com.aspose.words/htmlcontroltype/) لذلك العنصر. أمثلة: يوضح كيفية ضبط النوع المفضل لعقد المستند التي ستمثل العناصر المستوردة  و  العناصر.   final String html = "\\r\\n\\r\\n\\r\\n" + "item1\\r\\n\\r\\n\\r\\n\\r\\n"; HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions(); htmlLoadOptions.setPreferredControlType(HtmlControlType.STRUCTURED\_DOCUMENT\_TAG); Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF\_8)), htmlLoadOptions); NodeCollection nodes = doc.getChildNodes(NodeType.STRUCTURED\_DOCUMENT\_TAG, true); StructuredDocumentTag tag = (StructuredDocumentTag) nodes.get(0);

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | النوع المفضل لعقد المستند التي ستمثل العناصر المستوردة  و  العناصر. يجب أن تكون القيمة واحدة من ثوابت [HtmlControlType](../../com.aspose.words/htmlcontroltype/). |

### setPreserveIncludePictureField(boolean value) {#setPreserveIncludePictureField-boolean}
```
public void setPreserveIncludePictureField(boolean value)
```


يضبط ما إذا كان سيتم الحفاظ على حقل INCLUDEPICTURE عند قراءة صيغ Microsoft Word. القيمة الافتراضية هي false.

 **Remarks:** 

بشكل افتراضي، يتم تحويل حقل INCLUDEPICTURE إلى كائن شكل. يمكنك تجاوز ذلك إذا كنت بحاجة إلى الحفاظ على الحقل، على سبيل المثال، إذا رغبت في تحديثه برمجياً. لاحظ مع ذلك أن هذا النهج غير شائع في **Aspose.Words**. استخدمه على مسؤوليتك الخاصة.

أحد حالات الاستخدام الممكنة قد يكون استخدام MERGEFIELD كحقل فرعي لتغيير مسار مصدر الصورة ديناميكياً. في هذه الحالة تحتاج إلى الحفاظ على INCLUDEPICTURE في النموذج.

 **Examples:** 

يوضح كيفية الحفاظ على حقول INCLUDEPICTURE أو تجاهلها عند تحميل مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldIncludePicture includePicture = (FieldIncludePicture) builder.insertField(FieldType.FIELD_INCLUDE_PICTURE, true);
 includePicture.setSourceFullName(getImageDir() + "Transparent background logo.png");
 includePicture.update(true);

 try (ByteArrayOutputStream docStream = new ByteArrayOutputStream()) {
     doc.save(docStream, new OoxmlSaveOptions(SaveFormat.DOCX));

     // We can set a flag in a LoadOptions object to decide whether to convert all INCLUDEPICTURE fields
     // into image shapes when loading a document that contains them.
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setPreserveIncludePictureField(preserveIncludePictureField);
     }

     doc = new Document(new ByteArrayInputStream(docStream.toByteArray()), loadOptions);
     FieldCollection fieldCollection = doc.getRange().getFields();

     if (preserveIncludePictureField) {
         Assert.assertTrue(IterableUtils.matchesAny(fieldCollection, f -> f.getType() == FieldType.FIELD_INCLUDE_PICTURE));

         doc.updateFields();
         doc.save(getArtifactsDir() + "Field.PreserveIncludePicture.docx");
     } else {
         Assert.assertFalse(IterableUtils.matchesAny(fieldCollection, f -> f.getType() == FieldType.FIELD_INCLUDE_PICTURE));
     }
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | ما إذا كان سيتم الحفاظ على حقل INCLUDEPICTURE عند قراءة صيغ Microsoft Word. |

### setProgressCallback(IDocumentLoadingCallback value) {#setProgressCallback-com.aspose.words.IDocumentLoadingCallback}
```
public void setProgressCallback(IDocumentLoadingCallback value)
```


يُستدعى أثناء تحميل مستند ويقبل بيانات حول تقدم التحميل.

 **Remarks:** 

[LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX), [LoadFormat.FLAT\_OPC](../../com.aspose.words/loadformat/\#FLAT-OPC), [LoadFormat.DOCM](../../com.aspose.words/loadformat/\#DOCM), [LoadFormat.DOTM](../../com.aspose.words/loadformat/\#DOTM), [LoadFormat.DOTX](../../com.aspose.words/loadformat/\#DOTX), [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN), [LoadFormat.RTF](../../com.aspose.words/loadformat/\#RTF), [LoadFormat.WORD\_ML](../../com.aspose.words/loadformat/\#WORD-ML), [LoadFormat.DOC](../../com.aspose.words/loadformat/\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat/\#DOT), [LoadFormat.ODT](../../com.aspose.words/loadformat/\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat/\#OTT) formats supported.

 **Examples:** 

يوضح كيفية إبلاغ المستخدم إذا تجاوز تحميل المستند الوقت المتوقع للتحميل.

```

 public void progressCallback() throws Exception
 {
     LoadingProgressCallback progressCallback = new LoadingProgressCallback();

     LoadOptions loadOptions = new LoadOptions(); { loadOptions.setProgressCallback(progressCallback); }

     try
     {
         new Document(getMyDir() + "Big document.docx", loadOptions);
     }
     catch (IllegalStateException exception)
     {
         System.out.println(exception.getMessage());
         // Handle loading duration issue.
     }
 }

 /// 
 /// Cancel a document loading after the "MaxDuration" seconds.
 /// 
 public static class LoadingProgressCallback implements IDocumentLoadingCallback
 {
     /// 
     /// Ctr.
     /// 
     public LoadingProgressCallback()
     {
         mLoadingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document loading.
     /// 
     /// Loading arguments.
     public void notify(DocumentLoadingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mLoadingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document loading is started.
     /// 
     private Date mLoadingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.5;
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/) | القيمة المقابلة لـ [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/). |

### setRecoveryMode(int value) {#setRecoveryMode-int}
```
public void setRecoveryMode(int value)
```


يحدد كيفية معالجة المستند إذا حدثت أخطاء أثناء التحميل. استخدم هذه الخاصية لتحديد ما إذا كان النظام يجب أن يحاول استعادة المستند أو يتبع سلوكًا معرفًا آخر. القيمة الافتراضية هي [DocumentRecoveryMode.TRY\_RECOVER](../../com.aspose.words/documentrecoverymode/\#TRY-RECOVER).

 **Examples:** 

يوضح كيفية محاولة استعادة مستند إذا حدثت أخطاء أثناء التحميل.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setRecoveryMode(DocumentRecoveryMode.TRY_RECOVER);

 Document doc = new Document(getMyDir() + "Corrupted footnotes.docx", loadOptions);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة الصحيحة (int) المقابلة. يجب أن تكون القيمة واحدة من ثوابت [DocumentRecoveryMode](../../com.aspose.words/documentrecoverymode/). |

### setResourceLoadingCallback(IResourceLoadingCallback value) {#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback}
```
public void setResourceLoadingCallback(IResourceLoadingCallback value)
```


يسمح بالتحكم في كيفية تحميل الموارد الخارجية (الصور، أوراق الأنماط) عندما يتم استيراد مستند من HTML أو MHTML.

 **Examples:** 

يوضح كيفية معالجة الموارد الخارجية عند تحميل مستندات Html.

```

 public void loadOptionsCallback() throws Exception {
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setResourceLoadingCallback(new HtmlLinkedResourceLoadingCallback());

     // When we load the document, our callback will handle linked resources such as CSS stylesheets and images.
     Document doc = new Document(getMyDir() + "Images.html", loadOptions);
     doc.save(getArtifactsDir() + "LoadOptions.LoadOptionsCallback.pdf");
 }

 /// 
 /// Prints the filenames of all external stylesheets and substitutes all images of a loaded html document.
 /// 
 private static class HtmlLinkedResourceLoadingCallback implements IResourceLoadingCallback {
     public int resourceLoading(ResourceLoadingArgs args) throws IOException {
         switch (args.getResourceType()) {
             case ResourceType.CSS_STYLE_SHEET:
                 System.out.println(MessageFormat.format("External CSS Stylesheet found upon loading: {0}", args.getOriginalUri()));
                 return ResourceLoadingAction.DEFAULT;
             case ResourceType.IMAGE:
                 System.out.println(MessageFormat.format("External Image found upon loading: {0}", args.getOriginalUri()));

                 final String newImageFilename = "Logo.jpg";
                 System.out.println(MessageFormat.format("\tImage will be substituted with: {0}", newImageFilename));

                 byte[] imageBytes = FileUtils.readFileToByteArray(new File(getImageDir() + newImageFilename));
                 args.setData(imageBytes);

                 return ResourceLoadingAction.USER_PROVIDED;
         }

         return ResourceLoadingAction.DEFAULT;
     }
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) | القيمة المقابلة لـ [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/). |

### setSupportFontFaceRules(boolean value) {#setSupportFontFaceRules-boolean}
```
public void setSupportFontFaceRules(boolean value)
```


يضبط قيمة تشير إلى ما إذا كان سيتم دعم قواعد @font-face وما إذا كان سيتم تحميل الخطوط المعلنة. القيمة الافتراضية هي false.

 **Remarks:** 

إذا تم تمكين هذا الخيار، يتم تحميل الخطوط المعلنة في قواعد @font-face وتضمينها في تعريفات الخطوط للمستند الناتج (انظر [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/#getFontInfos)). يجعل ذلك الخطوط المحملة متاحة للعرض ولكن لا يفعّل تلقائيًا تضمين الخطوط عند الحفظ. من أجل حفظ المستند مع الخطوط المحملة، يجب تعيين خاصية [FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/#getEmbedTrueTypeFonts) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/#setEmbedTrueTypeFonts-boolean) في مجموعة [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/#getFontInfos) إلى true.

تنسيقات الخطوط المدعومة هي TTF و EOT و WOFF.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة تشير إلى ما إذا كان سيتم دعم قواعد @font-face وما إذا كان سيتم تحميل الخطوط المعلنة. |

### setSupportVml(boolean value) {#setSupportVml-boolean}
```
public void setSupportVml(boolean value)
```


يضبط قيمة تشير إلى ما إذا كان يجب دعم صور VML.

 **Examples:** 

يوضح كيفية دعم التعليقات الشرطية أثناء تحميل مستند HTML.

```

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();

 // If the value is true, then we take VML code into account while parsing the loaded document.
 loadOptions.setSupportVml(supportVml);

 // This document contains a JPEG image within "
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة تشير إلى ما إذا كان يجب دعم صور VML. |

### setTempFolder(String value) {#setTempFolder-java.lang.String}
```
public void setTempFolder(String value)
```


يسمح باستخدام ملفات مؤقتة عند قراءة المستند. بشكل افتراضي تكون هذه الخاصية null ولا يتم استخدام أي ملفات مؤقتة.

 **Remarks:** 

يجب أن يكون المجلد موجودًا وقابلًا للكتابة، وإلا سيتم رمي استثناء.

**Aspose.Words** تحذف تلقائيًا جميع الملفات المؤقتة عند اكتمال القراءة.

 **Examples:** 

يوضح كيفية تحميل مستند باستخدام ملفات مؤقتة.

```

 // Note that such an approach can reduce memory usage but degrades speed.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setTempFolder("C:\\TempFolder\\");

 // Ensure that the directory exists and load.
 new File(loadOptions.getTempFolder()).mkdir();

 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);
 
```

يوضح كيفية استخدام القرص الصلب بدلاً من الذاكرة عند تحميل مستند.

```

 // When we load a document, various elements are temporarily stored in memory as the save operation occurs.
 // We can use this option to use a temporary folder in the local file system instead,
 // which will reduce our application's memory overhead.
 LoadOptions options = new LoadOptions();
 options.setTempFolder(getArtifactsDir() + "TempFiles");

 // The specified temporary folder must exist in the local file system before the load operation.
 Files.createDirectory(Paths.get(options.getTempFolder()));

 Document doc = new Document(getMyDir() + "Document.docx", options);

 // The folder will persist with no residual contents from the load operation.
 Assert.assertTrue(DocumentHelper.directoryGetFiles(options.getTempFolder(), "*.*").size() == 0);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setUpdateDirtyFields(boolean value) {#setUpdateDirtyFields-boolean}
```
public void setUpdateDirtyFields(boolean value)
```


يحدد ما إذا كان يجب تحديث الحقول باستخدام السمة  dirty .

 **Examples:** 

يوضح كيفية استخدام الخاصية الخاصة لتحديث نتيجة الحقل.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Give the document's built-in "Author" property value, and then display it with a field.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 FieldAuthor field = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);

 Assert.assertFalse(field.isDirty());
 Assert.assertEquals("John Doe", field.getResult());

 // Update the property. The field still displays the old value.
 doc.getBuiltInDocumentProperties().setAuthor("John & Jane Doe");

 Assert.assertEquals("John Doe", field.getResult());

 // Since the field's value is out of date, we can mark it as "dirty".
 // This value will stay out of date until we update the field manually with the Field.Update() method.
 field.isDirty(true);

 // If we save without calling an update method,
 // the field will keep displaying the out of date value in the output document.
 doc.save(getArtifactsDir() + "Filed.UpdateDirtyFields.docx");

 // The LoadOptions object has an option to update all fields
 // marked as "dirty" when loading the document.
 LoadOptions options = new LoadOptions();
 options.setUpdateDirtyFields(updateDirtyFields);

 doc = new Document(getArtifactsDir() + "Filed.UpdateDirtyFields.docx", options);

 Assert.assertEquals("John & Jane Doe", doc.getBuiltInDocumentProperties().getAuthor());

 field = (FieldAuthor) doc.getRange().getFields().get(0);

 // Updating dirty fields like this automatically set their "IsDirty" flag to false.
 if (updateDirtyFields) {
     Assert.assertEquals("John & Jane Doe", field.getResult());
     Assert.assertFalse(field.isDirty());
 } else {
     Assert.assertEquals("John Doe", field.getResult());
     Assert.assertTrue(field.isDirty());
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setUseSystemLcid(boolean value) {#setUseSystemLcid-boolean}
```
public void setUseSystemLcid(boolean value)
```


يضبط ما إذا كان يجب استخدام قيمة LCID المستخرجة من سجل Windows لتحديد هوامش إعداد الصفحة الافتراضية.

 **Remarks:** 

إذا تم تعيينه إلى true، يتم محاكاة سلوك MS Word الذي يأخذ قيمة LCID من سجل Windows.

القيمة الافتراضية هي false.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | ما إذا كان يجب استخدام قيمة LCID المستخرجة من سجل Windows لتحديد هوامش إعداد الصفحة الافتراضية. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


يُستدعى أثناء عملية التحميل، عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق.

 **Examples:** 

يوضح كيفية طباعة وتخزين التحذيرات التي تحدث أثناء تحميل المستند.

```

 public void loadOptionsWarningCallback() throws Exception {
     // Create a new LoadOptions object and set its WarningCallback attribute
     // as an instance of our IWarningCallback implementation.
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setWarningCallback(new DocumentLoadingWarningCallback());

     // Our callback will print all warnings that come up during the load operation.
     Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

     ArrayList warnings = ((DocumentLoadingWarningCallback)loadOptions.getWarningCallback()).getWarnings();
     Assert.assertEquals(2, warnings.size());
 }

 /// 
 /// IWarningCallback that prints warnings and their details as they arise during document loading.
 /// 
 private static class DocumentLoadingWarningCallback implements IWarningCallback {
     public void warning(WarningInfo info) {
         System.out.println(MessageFormat.format("Warning: {0}", info.getWarningType()));
         System.out.println(MessageFormat.format("\tSource: {0}", info.getSource()));
         System.out.println(MessageFormat.format("\tDescription: {0}", info.getDescription()));
         mWarnings.add(info);
     }

     public ArrayList getWarnings() {
         return mWarnings;
     }

     private final  ArrayList mWarnings = new ArrayList();
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | القيمة المقابلة لـ [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

### setWebRequestTimeout(int value) {#setWebRequestTimeout-int}
```
public void setWebRequestTimeout(int value)
```


عدد المللي ثانية للانتظار قبل انتهاء مهلة طلب الويب. القيمة الافتراضية هي 100000 مللي ثانية (100 ثانية).

 **Remarks:** 

عدد المللي ثانية التي تنتظرها **Aspose.Words** للحصول على استجابة عند تحميل الموارد الخارجية (الصور، أوراق الأنماط) المرتبطة في مستندات HTML و MHTML.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | القيمة  int  المقابلة. |

