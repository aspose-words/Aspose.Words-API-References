---
title: FileFormatInfo.HasDigitalSignature
linktitle: HasDigitalSignature
articleTitle: HasDigitalSignature
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FileFormatInfo HasDigitalSignature—تحقق بسرعة مما إذا كانت مستندك تتضمن توقيعًا رقميًا، مما يعزز الأمان والمصداقية.
type: docs
weight: 20
url: /ar/net/aspose.words/fileformatinfo/hasdigitalsignature/
---
## FileFormatInfo.HasDigitalSignature property

إرجاع`حقيقي`إذا كان هذا المستند يحتوي على توقيع رقمي. هذه الخاصية تخبر فقط أن التوقيع الرقمي موجود على المستند، ولكنها لا تحدد ما إذا كان التوقيع صالحًا أم لا.

```csharp
public bool HasDigitalSignature { get; }
```

## ملاحظات

هذه الخاصية مصممة لمساعدتك على فرز المستندات الموقعة رقميًا عن غير الموقعة. إذا استخدمت Aspose.Words لتعديل وحفظ مستند موقع رقميًا، فسيتم فقدان التوقيع الرقمي. هذا مصمم لحماية صحة المستند، لأن التوقيع الرقمي موجود لحماية صحة المستند. باستخدام هذه الخاصية، يمكنك اكتشاف المستندات الموقعة رقميًا قبل معالجتها بنفس طريقة معالجة المستندات العادية، واتخاذ بعض الإجراءات لتجنب فقدان التوقيع الرقمي، مثل إخطار المستخدم.

## أمثلة

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

* class [FileFormatInfo](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
