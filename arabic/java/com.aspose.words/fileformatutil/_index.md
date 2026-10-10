---
title: "FileFormatUtil"
linktitle: "FileFormatUtil"
second_title: "Aspose.Words لـ Java"
description: "يوفر طرقًا مساعدة للعمل مع تنسيقات الملفات مثل اكتشاف تنسيق الملف أو تحويل امتدادات الملفات إلى/من تعداد تنسيقات الملفات في جافا."
type: docs
weight: 310
url: /ar/java/com.aspose.words/fileformatutil/
---

**Inheritance:**
java.lang.Object
```
public class FileFormatUtil
```

يوفر طرقًا مساعدة للعمل مع تنسيقات الملفات، مثل اكتشاف تنسيق الملف أو تحويل امتدادات الملفات إلى/من تعداد تنسيقات الملفات.

للتعرف على المزيد، زر مقالة الوثائق [ Detect File Format and Check Format Compatibility ][Detect File Format and Check Format Compatibility].

 **Examples:** 

يعرض كيفية اكتشاف الترميز في ملف HTML.

```

 FileFormatInfo info = FileFormatUtil.detectFileFormat(getMyDir() + "Document.html");

 Assert.assertEquals(LoadFormat.HTML, info.getLoadFormat());

 // The Encoding property is used only when we create a FileFormatInfo object for an html document.
 Assert.assertEquals("windows-1252", info.getEncoding().name());
 
```


[Detect File Format and Check Format Compatibility]: https://docs.aspose.com/words/java/detect-file-format-and-check-format-compatibility/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [contentTypeToLoadFormat(String contentType)](#contentTypeToLoadFormat-java.lang.String) | يحوّل نوع محتوى IANA إلى قيمة تعداد تنسيق التحميل. |
| [contentTypeToSaveFormat(String contentType)](#contentTypeToSaveFormat-java.lang.String) | يحوّل نوع محتوى IANA إلى قيمة تعداد تنسيق الحفظ. |
| [detectFileFormat(InputStream stream)](#detectFileFormat-java.io.InputStream) |  |
| [detectFileFormat(String fileName)](#detectFileFormat-java.lang.String) | يكشف ويعيد المعلومات حول تنسيق المستند. |
| [extensionToSaveFormat(String extension)](#extensionToSaveFormat-java.lang.String) | يحوّل امتداد اسم الملف إلى قيمة [SaveFormat](../../com.aspose.words/saveformat/). |
| [imageTypeToExtension(int imageType)](#imageTypeToExtension-int) |  |
| [loadFormatToExtension(int loadFormat)](#loadFormatToExtension-int) |  |
| [loadFormatToSaveFormat(int loadFormat)](#loadFormatToSaveFormat-int) |  |
| [saveFormatToExtension(int saveFormat)](#saveFormatToExtension-int) |  |
| [saveFormatToLoadFormat(int saveFormat)](#saveFormatToLoadFormat-int) |  |
### contentTypeToLoadFormat(String contentType) {#contentTypeToLoadFormat-java.lang.String}
```
public static int contentTypeToLoadFormat(String contentType)
```


يحوّل نوع محتوى IANA إلى قيمة تعداد تنسيق التحميل.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| contentType | java.lang.String |  |

**Returns:**
int
### contentTypeToSaveFormat(String contentType) {#contentTypeToSaveFormat-java.lang.String}
```
public static int contentTypeToSaveFormat(String contentType)
```


يحوّل نوع محتوى IANA إلى قيمة تعداد تنسيق الحفظ.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| contentType | java.lang.String |  |

**Returns:**
int
### detectFileFormat(InputStream stream) {#detectFileFormat-java.io.InputStream}
```
public static FileFormatInfo detectFileFormat(InputStream stream)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| stream | java.io.InputStream |  |

**Returns:**
[FileFormatInfo](../../com.aspose.words/fileformatinfo/)
### detectFileFormat(String fileName) {#detectFileFormat-java.lang.String}
```
public static FileFormatInfo detectFileFormat(String fileName)
```


يكشف ويعيد المعلومات حول تنسيق المستند.  يكشف ويعيد المعلومات حول تنسيق المستند المخزن في ملف على القرص.

 **Remarks:** 

حتى إذا اكتشف هذا الأسلوب تنسيق المستند، فإنه لا يضمن أن المستند المحدد صالح. يكتشف هذا الأسلوب تنسيق المستند فقط عن طريق قراءة البيانات الكافية للاكتشاف. للتحقق الكامل من صلاحية المستند، تحتاج إلى تحميل المستند إلى كائن [Document](../../com.aspose.words/document/).

يرمي هذا الأسلوب استثناء [FileCorruptedException](../../com.aspose.words/filecorruptedexception/) عندما يتم التعرف على التنسيق، لكن الكشف لا يمكن إكماله بسبب الفساد.

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fileName | java.lang.String | اسم الملف. |

**Returns:**
[FileFormatInfo](../../com.aspose.words/fileformatinfo/) - A [FileFormatInfo](../../com.aspose.words/fileformatinfo/) object that contains the detected information.
### extensionToSaveFormat(String extension) {#extensionToSaveFormat-java.lang.String}
```
public static int extensionToSaveFormat(String extension)
```


يحوّل امتداد اسم الملف إلى قيمة [SaveFormat](../../com.aspose.words/saveformat/).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| extension | java.lang.String | امتداد الملف. يمكن أن يكون مع أو بدون نقطة في البداية. غير حساس لحالة الأحرف. |

**Returns:**
int
### imageTypeToExtension(int imageType) {#imageTypeToExtension-int}
```
public static String imageTypeToExtension(int imageType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| imageType | int |  |

**Returns:**
java.lang.String
### loadFormatToExtension(int loadFormat) {#loadFormatToExtension-int}
```
public static String loadFormatToExtension(int loadFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| loadFormat | int |  |

**Returns:**
java.lang.String
### loadFormatToSaveFormat(int loadFormat) {#loadFormatToSaveFormat-int}
```
public static int loadFormatToSaveFormat(int loadFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| loadFormat | int |  |

**Returns:**
int
### saveFormatToExtension(int saveFormat) {#saveFormatToExtension-int}
```
public static String saveFormatToExtension(int saveFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
### saveFormatToLoadFormat(int saveFormat) {#saveFormatToLoadFormat-int}
```
public static int saveFormatToLoadFormat(int saveFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
int
