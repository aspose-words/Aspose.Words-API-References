---
title: DigitalSignatureDetails.CertificateHolder
linktitle: CertificateHolder
articleTitle: CertificateHolder
second_title: Aspose.Words для .NET
description: Откройте для себя свойство DigitalSignatureDetails CertificateHolder, чтобы без труда управлять сертификатом подписи вашего документа. Повысьте безопасность и оптимизируйте процессы!
type: docs
weight: 20
url: /ru/net/aspose.words.saving/digitalsignaturedetails/certificateholder/
---
## DigitalSignatureDetails.CertificateHolder property

Получает или задает`CertificateHolder` объект, содержащий сертификат, используемый для подписи документа.

```csharp
public CertificateHolder CertificateHolder { get; set; }
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

* class [CertificateHolder](../../../aspose.words.digitalsignatures/certificateholder/)
* class [DigitalSignatureDetails](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
