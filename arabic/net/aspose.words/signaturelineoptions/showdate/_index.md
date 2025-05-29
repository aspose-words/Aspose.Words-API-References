---
title: SignatureLineOptions.ShowDate
linktitle: ShowDate
articleTitle: ShowDate
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية ShowDate في SignatureLineOptions على تعزيز احترافية مستندك من خلال عرض تاريخ التوقيع على أسطر التوقيع.
type: docs
weight: 60
url: /ar/net/aspose.words/signaturelineoptions/showdate/
---
## SignatureLineOptions.ShowDate property

يحصل على قيمة أو يعينها تشير إلى أن تاريخ التوقيع يظهر في سطر التوقيع. القيمة الافتراضية لهذه الخاصية هي`حقيقي` .

```csharp
public bool ShowDate { get; set; }
```

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

* class [SignatureLineOptions](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
