---
title: FileFormatInfo.HasDigitalSignature
second_title: Aspose.Words لمراجع .NET API
description: FileFormatInfo ملكية. إرجاعحقيقيإذا كان هذا المستند يحتوي على توقيع رقمي. تشير هذه الخاصية فقط إلى وجود توقيع رقمي في المستند ولكنها لا تحدد ما إذا كان التوقيع صالحًا أم لا.
type: docs
weight: 20
url: /ar/net/aspose.words/fileformatinfo/hasdigitalsignature/
---
## FileFormatInfo.HasDigitalSignature property

إرجاع`حقيقي`إذا كان هذا المستند يحتوي على توقيع رقمي. تشير هذه الخاصية فقط إلى وجود توقيع رقمي في المستند، ولكنها لا تحدد ما إذا كان التوقيع صالحًا أم لا.

```csharp
public bool HasDigitalSignature { get; }
```

### ملاحظات

توجد هذه الخاصية لمساعدتك في فرز المستندات الموقعة رقميًا عن المستندات غير الموقعة. إذا كنت تستخدم Aspose.Words لتعديل وحفظ مستند موقع رقميًا، فسيتم فقدان التوقيع الرقمي . وهذا حسب التصميم نظرًا لوجود توقيع رقمي لحماية صحة المستند. باستخدام هذه الخاصية، يمكنك اكتشاف المستندات الموقعة رقميًا قبل معالجتها بنفس طريقة التعامل مع المستندات العادية واتخاذ بعض الإجراءات لتجنب فقدان التوقيع الرقمي، على سبيل المثال إعلام المستخدم.

### أمثلة

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

* class [FileFormatInfo](../)
* مساحة الاسم [Aspose.Words](../../fileformatinfo/)
* المجسم [Aspose.Words](../../../)


