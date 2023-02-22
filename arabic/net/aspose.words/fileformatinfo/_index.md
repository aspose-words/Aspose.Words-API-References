---
title: Class FileFormatInfo
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.FileFormatInfo فصل. يحتوي على بيانات تم إرجاعها بواسطةFileFormatUtil طرق الكشف عن تنسيق المستند.
type: docs
weight: 2630
url: /ar/net/aspose.words/fileformatinfo/
---
## FileFormatInfo class

يحتوي على بيانات تم إرجاعها بواسطة[`FileFormatUtil`](../fileformatutil/) طرق الكشف عن تنسيق المستند.

```csharp
public class FileFormatInfo
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Encoding](../../aspose.words/fileformatinfo/encoding/) { get; } | يحصل على الترميز الذي تم اكتشافه إذا كان مناسبًا لتنسيق المستند الحالي. في الوقت الحالي يكتشف الترميز لمستندات HTML فقط. |
| [HasDigitalSignature](../../aspose.words/fileformatinfo/hasdigitalsignature/) { get; } | يتم إرجاع صحيح إذا كان هذا المستند يحتوي على توقيع رقمي. تخبر هذه الخاصية فقط بوجود توقيع رقمي على المستند ، ولكنها لا تحدد ما إذا كان التوقيع صالحًا أم لا. |
| [IsEncrypted](../../aspose.words/fileformatinfo/isencrypted/) { get; } | يتم إرجاع صحيح إذا كان المستند مشفرًا ويتطلب كلمة مرور للفتح. |
| [LoadFormat](../../aspose.words/fileformatinfo/loadformat/) { get; } | يحصل على تنسيق المستند المكتشف. |

### ملاحظات

لا تقوم بإنشاء نسخ من هذه الفئة مباشرة. يتم إرجاع كائنات هذه الفئة بواسطة [`DetectFileFormat`](../fileformatutil/detectfileformat/)طُرق.

### أمثلة

يوضح كيفية استخدام فئة FileFormatUtil لاكتشاف تنسيق المستند وتشفيره.

```csharp
Document doc = new Document();

// تكوين كائن SaveOptions لتشفير المستند
// بكلمة مرور عندما نحفظها ، ثم نحفظ المستند.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// تحقق من نوع ملف وثيقتنا ، وحالة تشفيرها.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

يوضح كيفية استخدام فئة FileFormatUtil لاكتشاف تنسيق المستند ووجود التوقيعات الرقمية.

```csharp
// استخدم مثيل FileFormatInfo للتحقق من عدم توقيع المستند رقميًا.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, new SignOptions() { SignTime = DateTime.Now });

// استخدم FileFormatInstance جديدًا لتأكيد توقيعه.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// يمكننا تحميل والوصول إلى توقيعات وثيقة موقعة في مجموعة مثل هذه.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


