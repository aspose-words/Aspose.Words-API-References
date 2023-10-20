---
title: SignatureLineOptions.AllowComments
linktitle: AllowComments
articleTitle: AllowComments
second_title: Aspose.Words для .NET
description: SignatureLineOptions AllowComments свойство. Получает или задает значение указывающее что подписывающая сторона может добавлять комментарии в диалоговом окне Подпись. Значение по умолчанию для этого свойстваЛОЖЬ  на С#.
type: docs
weight: 20
url: /ru/net/aspose.words/signaturelineoptions/allowcomments/
---
## SignatureLineOptions.AllowComments property

Получает или задает значение, указывающее, что подписывающая сторона может добавлять комментарии в диалоговом окне «Подпись». Значение по умолчанию для этого свойства:`ЛОЖЬ` .

```csharp
public bool AllowComments { get; set; }
```

## Примеры

Показывает, как подписать документ личным удостоверением и строкой подписи.

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

// Снова открываем сохраненный документ и проверяем, что свойства «IsSigned» и «IsValid» равны «true»,
// указываем, что строка подписи содержит подпись.
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.True(signatureLine.IsSigned);
Assert.True(signatureLine.IsValid);
```

### Смотрите также

* class [SignatureLineOptions](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
