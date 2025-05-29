---
title: SignatureLineOptions Class
linktitle: SignatureLineOptions
articleTitle: SignatureLineOptions
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.SignatureLineOptions, чтобы легко настраивать линии подписи в ваших документах. Улучшите свой опыт DocumentBuilder сегодня!
type: docs
weight: 6940
url: /ru/net/aspose.words/signaturelineoptions/
---
## SignatureLineOptions class

Позволяет указать параметры для вставляемой строки подписи. Используется в[`DocumentBuilder`](../documentbuilder/) .

Чтобы узнать больше, посетите[Работа с цифровыми подписями](https://docs.aspose.com/words/net/working-with-digital-signatures/) документальная статья.

```csharp
public class SignatureLineOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [SignatureLineOptions](signaturelineoptions/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AllowComments](../../aspose.words/signaturelineoptions/allowcomments/) { get; set; } | Возвращает или задает значение, указывающее, может ли подписывающая сторона добавлять комментарии в диалоговом окне «Подписание». Значение по умолчанию для этого свойства —`ЛОЖЬ` . |
| [DefaultInstructions](../../aspose.words/signaturelineoptions/defaultinstructions/) { get; set; } | Возвращает или задает значение, указывающее, что в диалоговом окне «Подписать» отображаются инструкции по умолчанию. Значение по умолчанию для этого свойства:`истинный` . |
| [Email](../../aspose.words/signaturelineoptions/email/) { get; set; } | Возвращает или задает адрес электронной почты предполагаемого подписчика. Значение по умолчанию для этого свойства:**пустая строка** (Empty ). |
| [Instructions](../../aspose.words/signaturelineoptions/instructions/) { get; set; } | Возвращает или задает инструкции для подписывающего, которые отображаются при подписании строки подписи. Значение по умолчанию для этого свойства:**пустая строка** (Empty ). |
| [ShowDate](../../aspose.words/signaturelineoptions/showdate/) { get; set; } | Возвращает или задает значение, указывающее, отображается ли дата подписи в строке подписи. Значение по умолчанию для этого свойства:`истинный` . |
| [Signer](../../aspose.words/signaturelineoptions/signer/) { get; set; } | Возвращает или задает предлагаемого подписчика строки подписи. Значение по умолчанию для этого свойства:**пустая строка** (Empty ). |
| [SignerTitle](../../aspose.words/signaturelineoptions/signertitle/) { get; set; } | Возвращает или задает предлагаемую должность подписчика. Значение по умолчанию для этого свойства:**пустая строка** (Empty ). |

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
