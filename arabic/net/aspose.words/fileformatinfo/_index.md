---
title: Class FileFormatInfo
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.FileFormatInfo فصل. يحتوي على البيانات التي تم إرجاعها بواسطةFileFormatUtil طرق الكشف عن تنسيق المستند.
type: docs
weight: 2810
url: /ar/net/aspose.words/fileformatinfo/
---
## FileFormatInfo class

يحتوي على البيانات التي تم إرجاعها بواسطة[`FileFormatUtil`](../fileformatutil/) طرق الكشف عن تنسيق المستند.

لمعرفة المزيد، قم بزيارة[كشف تنسيق الملف والتحقق من توافق التنسيق](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) مقالة توثيقية.

```csharp
public class FileFormatInfo
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Encoding](../../aspose.words/fileformatinfo/encoding/) { get; } | يحصل على الترميز المكتشف إذا كان قابلاً للتطبيق على تنسيق المستند الحالي. في الوقت الحالي يكتشف الترميز فقط لمستندات HTML. |
| [HasDigitalSignature](../../aspose.words/fileformatinfo/hasdigitalsignature/) { get; } | إرجاع`حقيقي`إذا كان هذا المستند يحتوي على توقيع رقمي. تشير هذه الخاصية فقط إلى وجود توقيع رقمي في المستند، ولكنها لا تحدد ما إذا كان التوقيع صالحًا أم لا. |
| [IsEncrypted](../../aspose.words/fileformatinfo/isencrypted/) { get; } | إرجاع`حقيقي` إذا كان المستند مشفرًا ويتطلب كلمة مرور لفتحه. |
| [LoadFormat](../../aspose.words/fileformatinfo/loadformat/) { get; } | الحصول على تنسيق المستند الذي تم اكتشافه. |

### ملاحظات

لا تقم بإنشاء مثيلات هذه الفئة مباشرة. يتم إرجاع كائنات هذه الفئة بواسطة [`DetectFileFormat`](../fileformatutil/detectfileformat/) طُرق.

### أمثلة

يوضح كيفية استخدام فئة FileFormatUtil للكشف عن تنسيق المستند وتشفيره.

```csharp
Document doc = new Document();

// قم بتكوين كائن SaveOptions لتشفير المستند
// بكلمة مرور عندما نحفظها، ثم نحفظ المستند.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// تحقق من نوع ملف وثيقتنا وحالة التشفير الخاصة به.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

يوضح كيفية استخدام فئة FileFormatUtil للكشف عن تنسيق المستند ووجود التوقيعات الرقمية.

```csharp
// استخدم مثيل FileFormatInfo للتحقق من عدم توقيع المستند رقميًا.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, new SignOptions() { SignTime = DateTime.Now });

// استخدم FileFormatInstance جديد لتأكيد توقيعه.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// يمكننا تحميل التوقيعات الخاصة بالمستند الموقع في مجموعة كهذه والوصول إليها.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


