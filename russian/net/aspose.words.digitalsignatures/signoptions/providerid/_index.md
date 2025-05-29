---
title: SignOptions.ProviderId
linktitle: ProviderId
articleTitle: ProviderId
second_title: Aspose.Words для .NET
description: Откройте для себя свойство SignOptions ProviderId, определяющее идентификатор класса вашего поставщика подписи. Легко настраивайте с помощью уникального GUID для оптимальной производительности.
type: docs
weight: 40
url: /ru/net/aspose.words.digitalsignatures/signoptions/providerid/
---
## SignOptions.ProviderId property

Указывает идентификатор класса поставщика подписи. Значение по умолчанию:**Пусто (все нули) Guid** .

```csharp
public Guid ProviderId { get; set; }
```

## Примечания

Поставщик криптографических услуг (CSP) — это независимый программный модуль, который фактически выполняет алгоритмы криптографии для аутентификации, кодирования и шифрования. MS Office резервирует значение {00000000-0000-0000-0000-0000000000000} для своего поставщика подписей по умолчанию.

GUID дополнительно установленного поставщика следует получить из документации, поставляемой вместе с поставщиком.

Кроме того, все установленные поставщики криптографии перечислены в реестре Windows. Его можно найти по следующему пути: HKLM\SOFTWARE\Microsoft\Cryptography\Defaults\Provider. Существует ключевое имя «CP Service UUID», которое соответствует GUID поставщика подписей.

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

* class [SignOptions](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* сборка [Aspose.Words](../../../)
