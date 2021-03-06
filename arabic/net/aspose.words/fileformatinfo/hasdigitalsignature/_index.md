---
title: HasDigitalSignature
second_title: Aspose.Words لمراجع .NET API
description: يتم إرجاع صحيح إذا كان هذا المستند يحتوي على توقيع رقمي. تخبر هذه الخاصية فقط بوجود توقيع رقمي على المستند  ولكنها لا تحدد ما إذا كان التوقيع صالحًا أم لا.
type: docs
weight: 20
url: /ar/net/aspose.words/fileformatinfo/hasdigitalsignature/
---
## FileFormatInfo.HasDigitalSignature property

يتم إرجاع صحيح إذا كان هذا المستند يحتوي على توقيع رقمي. تخبر هذه الخاصية فقط بوجود توقيع رقمي على المستند ، ولكنها لا تحدد ما إذا كان التوقيع صالحًا أم لا.

```csharp
public bool HasDigitalSignature { get; }
```

### ملاحظات

توجد هذه الخاصية لمساعدتك في فرز المستندات الموقعة رقميًا من تلك التي ليست موقعة. هذا حسب التصميم لأن التوقيع الرقمي موجود لحماية أصالة المستند. باستخدام هذه الخاصية ، يمكنك اكتشاف المستندات الموقعة رقميًا قبل معالجتها بنفس طريقة معالجة المستندات العادية واتخاذ بعض الإجراءات لتجنب فقدان التوقيع الرقمي ، على سبيل المثال إعلام المستخدم.

### أمثلة

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

* class [FileFormatInfo](../../fileformatinfo)
* مساحة الاسم [Aspose.Words](../../fileformatinfo)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
