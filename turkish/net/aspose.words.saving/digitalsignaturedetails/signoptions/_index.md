---
title: DigitalSignatureDetails.SignOptions
linktitle: SignOptions
articleTitle: SignOptions
second_title: .NET için Aspose.Words
description: DigitalSignatureDetails SignOptions özelliğinin, sorunsuz dijital imzalar için imzalama seçeneklerini kolayca yöneterek belge güvenliğini nasıl artırdığını keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/digitalsignaturedetails/signoptions/
---
## DigitalSignatureDetails.SignOptions property

Bir değeri alır veya ayarlar`SignOptions` Bir belgeyi imzalamak için kullanılan nesne.

```csharp
public SignOptions SignOptions { get; set; }
```

## Örnekler

OOXML belgesinin nasıl imzalanacağını gösterir.

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

### Ayrıca bakınız

* class [SignOptions](../../../aspose.words.digitalsignatures/signoptions/)
* class [DigitalSignatureDetails](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
