---
title: "FileFormatInfo"
linktitle: "FileFormatInfo"
second_title: "Aspose.Words لـ Java"
description: "يتضمن البيانات التي تُرجعها طرق اكتشاف تنسيق المستند في FileFormatUtil في جافا."
type: docs
weight: 309
url: /ar/java/com.aspose.words/fileformatinfo/
---

**Inheritance:**
java.lang.Object
```
public class FileFormatInfo
```

يتضمن البيانات التي تُرجعها طرق اكتشاف تنسيق المستند في [FileFormatUtil](../../com.aspose.words/fileformatutil/).

للتعرف على المزيد، زر مقالة الوثائق [ Detect File Format and Check Format Compatibility ][Detect File Format and Check Format Compatibility].

 **Remarks:** 

أنت لا تنشئ مثيلات من هذه الفئة مباشرة. يتم إرجاع كائنات هذه الفئة بواسطة طرق **M:Aspose.Words.FileFormatUtil.DetectFileFormat(System.IO.Stream)**.

 **Examples:** 

يعرض كيفية استخدام الفئة FileFormatUtil لاكتشاف تنسيق المستند والتشفير.

```

 Document doc = new Document();

 // Configure a SaveOptions object to encrypt the document
 // with a password when we save it, and then save the document.
 OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.ODT);
 saveOptions.setPassword("MyPassword");

 doc.save(getArtifactsDir() + "File.DetectDocumentEncryption.odt", saveOptions);

 // Verify the file type of our document, and its encryption status.
 FileFormatInfo info = FileFormatUtil.detectFileFormat(getArtifactsDir() + "File.DetectDocumentEncryption.odt");

 Assert.assertEquals(".odt", FileFormatUtil.loadFormatToExtension(info.getLoadFormat()));
 Assert.assertTrue(info.isEncrypted());
 
```

يعرض كيفية استخدام الفئة FileFormatUtil لاكتشاف تنسيق المستند ووجود التوقيعات الرقمية.

```

 // Use a FileFormatInfo instance to verify that a document is not digitally signed.
 FileFormatInfo info = FileFormatUtil.detectFileFormat(getMyDir() + "Document.docx");

 Assert.assertEquals(".docx", FileFormatUtil.loadFormatToExtension(info.getLoadFormat()));
 Assert.assertFalse(info.hasDigitalSignature());

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw", null);
 DigitalSignatureUtil.sign(getMyDir() + "Document.docx", getArtifactsDir() + "File.DetectDigitalSignatures.docx",
         certificateHolder);

 // Use a new FileFormatInstance to confirm that it is signed.
 info = FileFormatUtil.detectFileFormat(getArtifactsDir() + "File.DetectDigitalSignatures.docx");

 Assert.assertTrue(info.hasDigitalSignature());

 // We can load and access the signatures of a signed document in a collection like this.
 Assert.assertEquals(1, DigitalSignatureUtil.loadSignatures(getArtifactsDir() + "File.DetectDigitalSignatures.docx").getCount());
 
```


[Detect File Format and Check Format Compatibility]: https://docs.aspose.com/words/java/detect-file-format-and-check-format-compatibility/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getEncoding()](#getEncoding) | يحصل على الترميز المكتشف إذا كان ذلك مناسبًا لتنسيق المستند الحالي. |
| [getLoadFormat()](#getLoadFormat) | يحصل على تنسيق المستند المكتشف. |
| [hasDigitalSignature()](#hasDigitalSignature) | يرجع  true  إذا كان هذا المستند يحتوي على توقيع رقمي. |
| [hasMacros()](#hasMacros) | يرجع  true  إذا كان هذا المستند يحتوي على ماكرو VBA. |
| [isEncrypted()](#isEncrypted) | يرجع  true  إذا كان المستند مشفرًا ويتطلب كلمة مرور للفتح. |
### getEncoding() {#getEncoding}
```
public Charset getEncoding()
```


يحصل على الترميز المكتشف إذا كان ذلك مناسبًا لتنسيق المستند الحالي. في الوقت الحالي يكتشف الترميز فقط للمستندات HTML.

 **Examples:** 

يعرض كيفية اكتشاف الترميز في ملف HTML.

```

 FileFormatInfo info = FileFormatUtil.detectFileFormat(getMyDir() + "Document.html");

 Assert.assertEquals(LoadFormat.HTML, info.getLoadFormat());

 // The Encoding property is used only when we create a FileFormatInfo object for an html document.
 Assert.assertEquals("windows-1252", info.getEncoding().name());
 
```

**Returns:**
java.nio.charset.Charset - الترميز المكتشف إذا كان ذلك مناسبًا لتنسيق المستند الحالي.
### getLoadFormat() {#getLoadFormat}
```
public int getLoadFormat()
```


يحصل على تنسيق المستند المكتشف.

 **Remarks:** 

عند تشفير مستند OOXML، لا يمكن تحديد ما إذا كان مستند Excel أو Word أو PowerPoint دون فك تشفيره أولاً، لذا بالنسبة لمستند OOXML المشفر ستُعيد هذه الخاصية دائمًا [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX).

 **Examples:** 

يعرض كيفية استخدام الفئة FileFormatUtil لاكتشاف تنسيق المستند والتشفير.

```

 Document doc = new Document();

 // Configure a SaveOptions object to encrypt the document
 // with a password when we save it, and then save the document.
 OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.ODT);
 saveOptions.setPassword("MyPassword");

 doc.save(getArtifactsDir() + "File.DetectDocumentEncryption.odt", saveOptions);

 // Verify the file type of our document, and its encryption status.
 FileFormatInfo info = FileFormatUtil.detectFileFormat(getArtifactsDir() + "File.DetectDocumentEncryption.odt");

 Assert.assertEquals(".odt", FileFormatUtil.loadFormatToExtension(info.getLoadFormat()));
 Assert.assertTrue(info.isEncrypted());
 
```

يعرض كيفية استخدام الفئة FileFormatUtil لاكتشاف تنسيق المستند ووجود التوقيعات الرقمية.

```

 // Use a FileFormatInfo instance to verify that a document is not digitally signed.
 FileFormatInfo info = FileFormatUtil.detectFileFormat(getMyDir() + "Document.docx");

 Assert.assertEquals(".docx", FileFormatUtil.loadFormatToExtension(info.getLoadFormat()));
 Assert.assertFalse(info.hasDigitalSignature());

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw", null);
 DigitalSignatureUtil.sign(getMyDir() + "Document.docx", getArtifactsDir() + "File.DetectDigitalSignatures.docx",
         certificateHolder);

 // Use a new FileFormatInstance to confirm that it is signed.
 info = FileFormatUtil.detectFileFormat(getArtifactsDir() + "File.DetectDigitalSignatures.docx");

 Assert.assertTrue(info.hasDigitalSignature());

 // We can load and access the signatures of a signed document in a collection like this.
 Assert.assertEquals(1, DigitalSignatureUtil.loadSignatures(getArtifactsDir() + "File.DetectDigitalSignatures.docx").getCount());
 
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

**Returns:**
int - تنسيق المستند المكتشف. القيمة المرجعة هي واحدة من ثوابت [LoadFormat](../../com.aspose.words/loadformat/).
### hasDigitalSignature() {#hasDigitalSignature}
```
public boolean hasDigitalSignature()
```


يرجع  true  إذا كان هذا المستند يحتوي على توقيع رقمي. هذه الخاصية تُعلم فقط بوجود توقيع رقمي على المستند، لكنها لا تحدد ما إذا كان التوقيع صالحًا أم لا.

 **Remarks:** 

هذه الخاصية موجودة لمساعدتك في فرز المستندات الموقعة رقمياً عن تلك غير الموقعة. إذا استخدمت Aspose.Words لتعديل وحفظ مستند موقّع رقمياً، فسيُفقد التوقيع الرقمي. هذا مقصود لأن التوقيع الرقمي موجود لحماية أصالة المستند. باستخدام هذه الخاصية يمكنك اكتشاف المستندات الموقعة رقمياً قبل معالجتها بنفس طريقة المستندات العادية واتخاذ إجراء لتجنب فقدان التوقيع الرقمي، على سبيل المثال إبلاغ المستخدم.

 **Examples:** 

يعرض كيفية استخدام الفئة FileFormatUtil لاكتشاف تنسيق المستند ووجود التوقيعات الرقمية.

```

 // Use a FileFormatInfo instance to verify that a document is not digitally signed.
 FileFormatInfo info = FileFormatUtil.detectFileFormat(getMyDir() + "Document.docx");

 Assert.assertEquals(".docx", FileFormatUtil.loadFormatToExtension(info.getLoadFormat()));
 Assert.assertFalse(info.hasDigitalSignature());

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw", null);
 DigitalSignatureUtil.sign(getMyDir() + "Document.docx", getArtifactsDir() + "File.DetectDigitalSignatures.docx",
         certificateHolder);

 // Use a new FileFormatInstance to confirm that it is signed.
 info = FileFormatUtil.detectFileFormat(getArtifactsDir() + "File.DetectDigitalSignatures.docx");

 Assert.assertTrue(info.hasDigitalSignature());

 // We can load and access the signatures of a signed document in a collection like this.
 Assert.assertEquals(1, DigitalSignatureUtil.loadSignatures(getArtifactsDir() + "File.DetectDigitalSignatures.docx").getCount());
 
```

**Returns:**
boolean -  true  إذا كان هذا المستند يحتوي على توقيع رقمي.
### hasMacros() {#hasMacros}
```
public boolean hasMacros()
```


يرجع  true  إذا كان هذا المستند يحتوي على ماكرو VBA.

 **Examples:** 

يوضح كيفية التحقق من وجود ماكرو VBA دون تحميل المستند.

```

 FileFormatInfo fileFormatInfo = FileFormatUtil.detectFileFormat(getMyDir() + "Macro.docm");
 Assert.assertTrue(fileFormatInfo.hasMacros());
 
```

**Returns:**
boolean -  true  إذا كان هذا المستند يحتوي على ماكرو VBA.
### isEncrypted() {#isEncrypted}
```
public boolean isEncrypted()
```


يرجع  true  إذا كان المستند مشفرًا ويتطلب كلمة مرور للفتح.

 **Remarks:** 

هذه الخاصية موجودة لمساعدتك في فرز المستندات المشفرة عن غير المشفرة. إذا حاولت تحميل مستند مشفر باستخدام Aspose.Words دون توفير كلمة مرور، سيتم إلقاء استثناء. يمكنك استخدام هذه الخاصية لاكتشاف ما إذا كان المستند يتطلب كلمة مرور واتخاذ إجراء قبل تحميل المستند، على سبيل المثال طلب كلمة مرور من المستخدم.

 **Examples:** 

يعرض كيفية استخدام الفئة FileFormatUtil لاكتشاف تنسيق المستند والتشفير.

```

 Document doc = new Document();

 // Configure a SaveOptions object to encrypt the document
 // with a password when we save it, and then save the document.
 OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.ODT);
 saveOptions.setPassword("MyPassword");

 doc.save(getArtifactsDir() + "File.DetectDocumentEncryption.odt", saveOptions);

 // Verify the file type of our document, and its encryption status.
 FileFormatInfo info = FileFormatUtil.detectFileFormat(getArtifactsDir() + "File.DetectDocumentEncryption.odt");

 Assert.assertEquals(".odt", FileFormatUtil.loadFormatToExtension(info.getLoadFormat()));
 Assert.assertTrue(info.isEncrypted());
 
```

**Returns:**
boolean -  true  إذا كان المستند مشفرًا ويتطلب كلمة مرور للفتح.
