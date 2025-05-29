---
title: FileFormatInfo Class
linktitle: FileFormatInfo
articleTitle: FileFormatInfo
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.FileFormatInfo لاكتشاف تنسيقات المستندات بكفاءة. احصل على بيانات مفصلة لتحسين حلول إدارة الملفات لديك.
type: docs
weight: 3220
url: /ar/net/aspose.words/fileformatinfo/
---
## FileFormatInfo class

يحتوي على البيانات التي تم إرجاعها بواسطة[`FileFormatUtil`](../fileformatutil/) طرق الكشف عن تنسيق المستند.

لمعرفة المزيد، قم بزيارة[اكتشاف تنسيق الملف والتحقق من توافق التنسيق](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) مقالة توثيقية.

```csharp
public class FileFormatInfo
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Encoding](../../aspose.words/fileformatinfo/encoding/) { get; } | يحصل على الترميز المكتشف إذا كان ينطبق على تنسيق المستند الحالي. في الوقت الحالي يكتشف الترميز فقط لمستندات HTML. |
| [HasDigitalSignature](../../aspose.words/fileformatinfo/hasdigitalsignature/) { get; } | إرجاع`حقيقي`إذا كان هذا المستند يحتوي على توقيع رقمي. هذه الخاصية تخبر فقط أن التوقيع الرقمي موجود على المستند، ولكنها لا تحدد ما إذا كان التوقيع صالحًا أم لا. |
| [HasMacros](../../aspose.words/fileformatinfo/hasmacros/) { get; } | إرجاع`حقيقي` إذا كان هذا المستند يحتوي على وحدات ماكرو VBA. |
| [IsEncrypted](../../aspose.words/fileformatinfo/isencrypted/) { get; } | إرجاع`حقيقي` إذا تم تشفير المستند ويتطلب كلمة مرور لفتحه. |
| [LoadFormat](../../aspose.words/fileformatinfo/loadformat/) { get; } | يحصل على تنسيق المستند المكتشف. |

## ملاحظات

لا تُنشئ مثيلات لهذه الفئة مباشرةً. تُرجع كائنات هذه الفئة بواسطة [`DetectFileFormat`](../fileformatutil/detectfileformat/) طُرق.

## أمثلة

يوضح كيفية استخدام فئة FileFormatUtil لاكتشاف تنسيق المستند والتشفير.

```csharp
Document doc = new Document();

// تكوين كائن SaveOptions لتشفير المستند
// بكلمة مرور عندما نحفظه، ثم نحفظ المستند.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// التحقق من نوع الملف الخاص بمستندنا وحالة تشفيره.
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
SignOptions signOptions = new SignOptions() { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, signOptions);

// استخدم FileFormatInstance جديدًا للتأكد من توقيعه.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// يمكننا تحميل التوقيعات الخاصة بمستند موقّع والوصول إليها في مجموعة مثل هذه.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
