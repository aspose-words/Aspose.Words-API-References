---
title: OoxmlSaveOptions.DigitalSignatureDetails
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: Aspose.Words для .NET
description: Изучите свойство DigitalSignatureDetails OoxmlSaveOptions, чтобы эффективно управлять цифровыми подписями для безопасного подписания документов и повышения уровня соответствия требованиям.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/ooxmlsaveoptions/digitalsignaturedetails/
---
## OoxmlSaveOptions.DigitalSignatureDetails property

Получает или устанавливает[`DigitalSignatureDetails`](../../digitalsignaturedetails/) объект, используемый для подписи документа.

```csharp
public DigitalSignatureDetails DigitalSignatureDetails { get; set; }
```

## Примеры

Показывает, как подписывать документ OOXML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
DigitalSignatureDetails digitalSignatureDetails = new DigitalSignatureDetails(
    certificateHolder,
    new SignOptions() { Comments = "Some comments", SignTime = DateTime.Now });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.DigitalSignatureDetails = digitalSignatureDetails;

Assert.AreEqual(certificateHolder, digitalSignatureDetails.CertificateHolder);
Assert.AreEqual("Some comments", digitalSignatureDetails.SignOptions.Comments);

doc.Save(ArtifactsDir + "OoxmlSaveOptions.DigitalSignature.docx", saveOptions);
```

### Смотрите также

* class [DigitalSignatureDetails](../../digitalsignaturedetails/)
* class [OoxmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
