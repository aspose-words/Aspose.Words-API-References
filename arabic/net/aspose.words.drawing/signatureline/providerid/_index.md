---
title: SignatureLine.ProviderId
linktitle: ProviderId
articleTitle: ProviderId
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية SignatureLine ProviderId لإدارة مُعرّفات مُزوّد التوقيع بسهولة. بسّط سير عملك بإعداداتنا الافتراضية.
type: docs
weight: 80
url: /ar/net/aspose.words.drawing/signatureline/providerid/
---
## SignatureLine.ProviderId property

يحصل على معرف موفر التوقيع أو يعينه لسطر التوقيع هذا. القيمة الافتراضية هي "{00000000-0000-0000-0000-000000000000}".

```csharp
public Guid ProviderId { get; set; }
```

## ملاحظات

موفر خدمة التشفير (CSP) هو وحدة برمجية مستقلة تُجري فعليًا خوارزميات تشفير x000d_ للمصادقة والترميز والتشفير. يحتفظ MS Office بقيمة x000d_ {00000000-0000-0000-0000-00000000000} لموفر التوقيع الافتراضي.

يجب الحصول على GUID الخاص بالموفر المثبت بشكل إضافي من الوثائق المرفقة مع الموفر.

بالإضافة إلى ذلك، يتم تعداد جميع موفري التشفير المثبتين في سجل Windows. ويمكن العثور عليه في المسار التالي: HKLM\SOFTWARE\Microsoft\Cryptography\Defaults\Provider. يوجد اسم مفتاح "CP Service UUID" والذي يتوافق مع GUID لمزود التوقيع.

## أمثلة

يوضح كيفية توقيع مستند باستخدام شهادة شخصية وسطر التوقيع.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions signatureLineOptions = new SignatureLineOptions
{
    Signer = "vderyushev",
    SignerTitle = "QA",
    Email = "vderyushev@aspose.com",
    ShowDate = true,
    DefaultInstructions = false,
    Instructions = "Please sign here.",
    AllowComments = true
};

SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
signatureLine.ProviderId = Guid.Parse("CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2");

Assert.False(signatureLine.IsSigned);
Assert.False(signatureLine.IsValid);

doc.Save(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.docx");

SignOptions signOptions = new SignOptions
{
    SignatureLineId = signatureLine.Id,
    ProviderId = signatureLine.ProviderId,
    Comments = "Document was signed by vderyushev",
    SignTime = DateTime.Now
};

CertificateHolder certHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

DigitalSignatureUtil.Sign(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.docx", 
    ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

// أعد فتح المستند المحفوظ لدينا، وتأكد من أن الخاصيتين "IsSigned" و"IsValid" تساويان "true"،
// يشير إلى أن سطر التوقيع يحتوي على توقيع.
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.True(signatureLine.IsSigned);
Assert.True(signatureLine.IsValid);
```

### أنظر أيضا

* class [SignatureLine](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
