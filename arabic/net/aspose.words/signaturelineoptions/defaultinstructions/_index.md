---
title: SignatureLineOptions.DefaultInstructions
linktitle: DefaultInstructions
articleTitle: DefaultInstructions
second_title: Aspose.Words لـ .NET
description: SignatureLineOptions DefaultInstructions ملكية. الحصول على قيمة أو تعيينها تشير إلى أن التعليمات الافتراضية تظهر في مربع حوار التوقيع. القيمة الافتراضية لهذه الخاصية هيحقيقي  في C#.
type: docs
weight: 30
url: /ar/net/aspose.words/signaturelineoptions/defaultinstructions/
---
## SignatureLineOptions.DefaultInstructions property

الحصول على قيمة أو تعيينها تشير إلى أن التعليمات الافتراضية تظهر في مربع حوار التوقيع. القيمة الافتراضية لهذه الخاصية هي`حقيقي` .

```csharp
public bool DefaultInstructions { get; set; }
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

// أعد فتح المستند المحفوظ لدينا، وتحقق من أن الخاصيتين "IsSigned" و"IsValid" متساويتان للقيمة "true"،
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
