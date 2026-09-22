---
title: "ChmLoadOptions"
linktitle: "ChmLoadOptions"
second_title: "Aspose.Words لـ Java"
description: "يتيح تحديد خيارات إضافية عند تحميل مستند CHM إلى كائن Document في Java."
type: docs
weight: 102
url: /ar/java/com.aspose.words/chmloadoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.LoadOptions](../../com.aspose.words/loadoptions/)
```
public class ChmLoadOptions extends LoadOptions
```

يتيح تحديد خيارات إضافية عند تحميل مستند CHM إلى كائن [Document](../../com.aspose.words/document/).

لمزيد من المعلومات، زر مقالة الوثائق [ Specify Load Options ][Specify Load Options].

 **Examples:** 

يظهر كيفية حل عناوين URL مثل \"ms-its:myfile.chm::/index.htm\".

```

 // Our document contains URLs like "ms-its:amhelp.chm::....htm", but it has a different name,
 // so file links don't work after saving it to HTML.
 // We need to define the original filename in 'ChmLoadOptions' to avoid this behavior.
 ChmLoadOptions loadOptions = new ChmLoadOptions(); { loadOptions.setOriginalFileName("amhelp.chm"); }

 Document doc = new Document(new ByteArrayInputStream(Files.readAllBytes(Paths.get(getMyDir() + "Document with ms-its links.chm"))),
     loadOptions);

 doc.save(getArtifactsDir() + "ExChmLoadOptions.OriginalFileName.html");
 
```


[Specify Load Options]: https://docs.aspose.com/words/java/specify-load-options/
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [ChmLoadOptions()](#ChmLoadOptions) | يُهيئ نسخة جديدة من هذه الفئة بالقيم الافتراضية. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | يحدد ما إذا كان الكائن المحدد مساويًا في القيمة للكائن الحالي. |
| [getBaseUri()](#getBaseUri) | يحصل على السلسلة التي ستُستخدم لحل عناوين URI النسبية الموجودة في المستند إلى عناوين URI مطلقة عند الحاجة. |
| [getConvertMetafilesToPng()](#getConvertMetafilesToPng) | يحصل على ما إذا كان سيتم تحويل ملفات الميتا ( **F:Aspose.FileFormat.Wmf** أو **F:Aspose.FileFormat.Emf**) إلى تنسيق الصورة **F:Aspose.FileFormat.Png**. |
| [getConvertShapeToOfficeMath()](#getConvertShapeToOfficeMath) | يحصل على ما إذا كان سيتم تحويل الأشكال التي تحتوي على EquationXML إلى كائنات Office Math. |
| [getEncoding()](#getEncoding) | يحصل على الترميز الذي سيُستخدم لتحميل مستند HTML أو TXT أو CHM إذا لم يتم تحديد الترميز داخل المستند. |
| [getFontSettings()](#getFontSettings) | يسمح بتحديد إعدادات خطوط المستند. |
| [getIgnoreOleData()](#getIgnoreOleData) | يحدد ما إذا كان يجب تجاهل بيانات OLE. |
| [getLanguagePreferences()](#getLanguagePreferences) | يحصل على تفضيلات اللغة التي ستُستخدم عند تحميل المستند. |
| [getLoadFormat()](#getLoadFormat) | يحدد تنسيق المستند الذي سيتم تحميله. |
| [getMswVersion()](#getMswVersion) | يسمح بتحديد أن عملية تحميل المستند يجب أن تتطابق مع إصدار محدد من MS Word. |
| [getOriginalFileName()](#getOriginalFileName) | اسم ملف CHM. |
| [getPassword()](#getPassword) | يحصل على كلمة المرور لفتح مستند مشفر. |
| [getPreserveIncludePictureField()](#getPreserveIncludePictureField) | يحصل على ما إذا كان يجب الحفاظ على حقل INCLUDEPICTURE عند قراءة صيغ Microsoft Word. |
| [getProgressCallback()](#getProgressCallback) | يُستدعى أثناء تحميل مستند ويقبل بيانات حول تقدم التحميل. |
| [getRecoveryMode()](#getRecoveryMode) | يحدد كيفية التعامل مع المستند إذا حدثت أخطاء أثناء التحميل. |
| [getResourceLoadingCallback()](#getResourceLoadingCallback) | يسمح بالتحكم في كيفية تحميل الموارد الخارجية (الصور، أوراق الأنماط) عندما يتم استيراد مستند من HTML أو MHTML. |
| [getTempFolder()](#getTempFolder) | يسمح باستخدام ملفات مؤقتة عند قراءة المستند. |
| [getUpdateDirtyFields()](#getUpdateDirtyFields) | يحدد ما إذا كان يجب تحديث الحقول باستخدام السمة  dirty . |
| [getUseSystemLcid()](#getUseSystemLcid) | يحصل على ما إذا كان يجب استخدام قيمة LCID المستخرجة من سجل Windows لتحديد هوامش إعداد الصفحة الافتراضية. |
| [getWarningCallback()](#getWarningCallback) | يُستدعى أثناء عملية التحميل، عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق. |
| [setBaseUri(String value)](#setBaseUri-java.lang.String) | يضبط السلسلة التي ستُستخدم لحل عناوين URI النسبية الموجودة في المستند إلى عناوين URI مطلقة عند الحاجة. |
| [setConvertMetafilesToPng(boolean value)](#setConvertMetafilesToPng-boolean) | يضبط ما إذا كان يجب تحويل صور الميتافايل ( **F:Aspose.FileFormat.Wmf** أو **F:Aspose.FileFormat.Emf**) إلى تنسيق الصورة **F:Aspose.FileFormat.Png**. |
| [setConvertShapeToOfficeMath(boolean value)](#setConvertShapeToOfficeMath-boolean) | يضبط ما إذا كان يجب تحويل الأشكال التي تحتوي على EquationXML إلى كائنات Office Math. |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset) | يضبط الترميز الذي سيُستخدم لتحميل مستند HTML أو TXT أو CHM إذا لم يتم تحديد الترميز داخل المستند. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | يسمح بتحديد إعدادات خطوط المستند. |
| [setIgnoreOleData(boolean value)](#setIgnoreOleData-boolean) | يحدد ما إذا كان يجب تجاهل بيانات OLE. |
| [setLoadFormat(int value)](#setLoadFormat-int) | يحدد تنسيق المستند الذي سيتم تحميله. |
| [setMswVersion(int value)](#setMswVersion-int) | يسمح بتحديد أن عملية تحميل المستند يجب أن تتطابق مع إصدار محدد من MS Word. |
| [setOriginalFileName(String value)](#setOriginalFileName-java.lang.String) | اسم ملف CHM. |
| [setPassword(String value)](#setPassword-java.lang.String) | يضبط كلمة المرور لفتح مستند مشفر. |
| [setPreserveIncludePictureField(boolean value)](#setPreserveIncludePictureField-boolean) | يضبط ما إذا كان يجب الحفاظ على حقل INCLUDEPICTURE عند قراءة صيغ Microsoft Word. |
| [setProgressCallback(IDocumentLoadingCallback value)](#setProgressCallback-com.aspose.words.IDocumentLoadingCallback) | يُستدعى أثناء تحميل مستند ويقبل بيانات حول تقدم التحميل. |
| [setRecoveryMode(int value)](#setRecoveryMode-int) | يحدد كيفية التعامل مع المستند إذا حدثت أخطاء أثناء التحميل. |
| [setResourceLoadingCallback(IResourceLoadingCallback value)](#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback) | يسمح بالتحكم في كيفية تحميل الموارد الخارجية (الصور، أوراق الأنماط) عندما يتم استيراد مستند من HTML أو MHTML. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String) | يسمح باستخدام ملفات مؤقتة عند قراءة المستند. |
| [setUpdateDirtyFields(boolean value)](#setUpdateDirtyFields-boolean) | يحدد ما إذا كان يجب تحديث الحقول باستخدام السمة  dirty . |
| [setUseSystemLcid(boolean value)](#setUseSystemLcid-boolean) | يضبط ما إذا كان يجب استخدام قيمة LCID المستخرجة من سجل Windows لتحديد هوامش إعداد الصفحة الافتراضية. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | يُستدعى أثناء عملية التحميل، عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق. |
### ChmLoadOptions() {#ChmLoadOptions}
```
public ChmLoadOptions()
```


يُهيئ نسخة جديدة من هذه الفئة بالقيم الافتراضية.

 **Examples:** 

يظهر كيفية حل عناوين URL مثل \"ms-its:myfile.chm::/index.htm\".

```

 // Our document contains URLs like "ms-its:amhelp.chm::....htm", but it has a different name,
 // so file links don't work after saving it to HTML.
 // We need to define the original filename in 'ChmLoadOptions' to avoid this behavior.
 ChmLoadOptions loadOptions = new ChmLoadOptions(); { loadOptions.setOriginalFileName("amhelp.chm"); }

 Document doc = new Document(new ByteArrayInputStream(Files.readAllBytes(Paths.get(getMyDir() + "Document with ms-its links.chm"))),
     loadOptions);

 doc.save(getArtifactsDir() + "ExChmLoadOptions.OriginalFileName.html");
 
```

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
### getOriginalFileName() {#getOriginalFileName}
```
public String getOriginalFileName()
```


اسم ملف CHM. القيمة الافتراضية هي null.

 **Remarks:** 

قد تحتوي مستندات CHM على روابط تشير إلى نفس المستند باسم الملف. تدعم Aspose.Words هذه الروابط عادةً وتستخدم [Document.getOriginalFileName()](../../com.aspose.words/document/\#getOriginalFileName) للتحقق مما إذا كان الملف المشار إليه بالرابط هو الملف الذي يتم تحميله. إذا تم تحميل مستند من تدفق، يجب تحديد اسم الملف الأصلي صراحةً عبر هذه الخاصية، لأنه لا يمكن تحديده تلقائيًا.

إذا تم تحميل مستند CHM من ملف وتم تحديد قيمة غير فارغة لهذه الخاصية، فستأخذ هذه القيمة أولوية على الاسم الفعلي للملف المخزن في [Document.getOriginalFileName()](../../com.aspose.words/document/\#getOriginalFileName).

 **Examples:** 

يظهر كيفية حل عناوين URL مثل \"ms-its:myfile.chm::/index.htm\".

```

 // Our document contains URLs like "ms-its:amhelp.chm::....htm", but it has a different name,
 // so file links don't work after saving it to HTML.
 // We need to define the original filename in 'ChmLoadOptions' to avoid this behavior.
 ChmLoadOptions loadOptions = new ChmLoadOptions(); { loadOptions.setOriginalFileName("amhelp.chm"); }

 Document doc = new Document(new ByteArrayInputStream(Files.readAllBytes(Paths.get(getMyDir() + "Document with ms-its links.chm"))),
     loadOptions);

 doc.save(getArtifactsDir() + "ExChmLoadOptions.OriginalFileName.html");
 
```

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
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

### setOriginalFileName(String value) {#setOriginalFileName-java.lang.String}
```
public void setOriginalFileName(String value)
```


اسم ملف CHM. القيمة الافتراضية هي null.

 **Remarks:** 

قد تحتوي مستندات CHM على روابط تشير إلى نفس المستند باسم الملف. تدعم Aspose.Words هذه الروابط عادةً وتستخدم [Document.getOriginalFileName()](../../com.aspose.words/document/\#getOriginalFileName) للتحقق مما إذا كان الملف المشار إليه بالرابط هو الملف الذي يتم تحميله. إذا تم تحميل مستند من تدفق، يجب تحديد اسم الملف الأصلي صراحةً عبر هذه الخاصية، لأنه لا يمكن تحديده تلقائيًا.

إذا تم تحميل مستند CHM من ملف وتم تحديد قيمة غير فارغة لهذه الخاصية، فستأخذ هذه القيمة أولوية على الاسم الفعلي للملف المخزن في [Document.getOriginalFileName()](../../com.aspose.words/document/\#getOriginalFileName).

 **Examples:** 

يظهر كيفية حل عناوين URL مثل \"ms-its:myfile.chm::/index.htm\".

```

 // Our document contains URLs like "ms-its:amhelp.chm::....htm", but it has a different name,
 // so file links don't work after saving it to HTML.
 // We need to define the original filename in 'ChmLoadOptions' to avoid this behavior.
 ChmLoadOptions loadOptions = new ChmLoadOptions(); { loadOptions.setOriginalFileName("amhelp.chm"); }

 Document doc = new Document(new ByteArrayInputStream(Files.readAllBytes(Paths.get(getMyDir() + "Document with ms-its links.chm"))),
     loadOptions);

 doc.save(getArtifactsDir() + "ExChmLoadOptions.OriginalFileName.html");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

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

