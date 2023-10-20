---
title: SignatureLine.ProviderId
linktitle: ProviderId
articleTitle: ProviderId
second_title: Aspose.Words для .NET
description: SignatureLine ProviderId свойство. Получает или задает идентификатор поставщика подписи для этой строки подписи. Значение по умолчанию 00000000000000000000000000000000 на С#.
type: docs
weight: 80
url: /ru/net/aspose.words.drawing/signatureline/providerid/
---
## SignatureLine.ProviderId property

Получает или задает идентификатор поставщика подписи для этой строки подписи. Значение по умолчанию: «{00000000-0000-0000-0000-000000000000}».

```csharp
public Guid ProviderId { get; set; }
```

## Примечания

Поставщик криптографических услуг (CSP) — это независимый программный модуль, который фактически выполняет криптографические алгоритмы для аутентификации, кодирования и шифрования. MS Office резервирует значение value {00000000-0000-0000-0000-000000000000} для своего поставщика подписей по умолчанию.

GUID дополнительно установленного провайдера следует получить из документации, поставляемой вместе с провайдером.

Кроме того, все установленные поставщики шифрования перечислены в реестре Windows. Его можно найти по следующему пути: HKLM\SOFTWARE\Microsoft\Cryptography\Defaults\Provider. Существует имя ключа «UUID службы CP», которое соответствует GUID поставщика подписи.

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

* class [SignatureLine](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
