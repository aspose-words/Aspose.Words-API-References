---
title: SignatureLineOptions.Instructions
second_title: Aspose.Words لمراجع .NET API
description: SignatureLineOptions ملكية. الحصول على التعليمات أو تعيينها للموقِّع التي يتم عرضها عند توقيع سطر التوقيع. القيمة الافتراضية لهذه الخاصية هي سلسلة فارغة Empty  .
type: docs
weight: 50
url: /ar/net/aspose.words/signaturelineoptions/instructions/
---
## SignatureLineOptions.Instructions property

الحصول على التعليمات أو تعيينها للموقِّع التي يتم عرضها عند توقيع سطر التوقيع. القيمة الافتراضية لهذه الخاصية هي **سلسلة فارغة** (Empty ) .

```csharp
public string Instructions { get; set; }
```

### أمثلة

يوضح كيفية توقيع مستند بشهادة شخصية وسطر توقيع.

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

// أعد فتح المستند المحفوظ ، وتحقق من أن خصائص "IsSigned" و "IsValid" تساوي "true" ،
// يشير إلى أن سطر التوقيع يحتوي على توقيع.
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.True(signatureLine.IsSigned);
Assert.True(signatureLine.IsValid);
```

### أنظر أيضا

* class [SignatureLineOptions](../)
* مساحة الاسم [Aspose.Words](../../signaturelineoptions/)
* المجسم [Aspose.Words](../../../)


