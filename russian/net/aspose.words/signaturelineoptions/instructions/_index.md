---
title: SignatureLineOptions.Instructions
linktitle: Instructions
articleTitle: Instructions
second_title: Aspose.Words для .NET
description: Узнайте, как настроить SignatureLineOptions с четкими инструкциями для подписывающих, улучшая процесс подписания. Простая настройка с настройками по умолчанию.
type: docs
weight: 50
url: /ru/net/aspose.words/signaturelineoptions/instructions/
---
## SignatureLineOptions.Instructions property

Возвращает или задает инструкции для подписывающего, которые отображаются при подписании строки подписи. Значение по умолчанию для этого свойства:**пустая строка** (Empty ).

```csharp
public string Instructions { get; set; }
```

## Примеры

Показывает, как подписать документ с помощью личного сертификата и строки подписи.

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

// Повторно откройте наш сохраненный документ и убедитесь, что свойства «IsSigned» и «IsValid» равны «true»,
// указывая, что строка подписи содержит подпись.
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
