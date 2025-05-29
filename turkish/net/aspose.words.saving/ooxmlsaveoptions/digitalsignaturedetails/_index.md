---
title: OoxmlSaveOptions.DigitalSignatureDetails
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: .NET için Aspose.Words
description: Güvenli belge imzalama ve gelişmiş uyumluluk için dijital imzaları etkin bir şekilde yönetmek amacıyla OoxmlSaveOptions'ın DigitalSignatureDetails özelliğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/ooxmlsaveoptions/digitalsignaturedetails/
---
## OoxmlSaveOptions.DigitalSignatureDetails property

Alır veya ayarlar[`DigitalSignatureDetails`](../../digitalsignaturedetails/) Bir belgeyi imzalamak için kullanılan nesne.

```csharp
public DigitalSignatureDetails DigitalSignatureDetails { get; set; }
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

* class [DigitalSignatureDetails](../../digitalsignaturedetails/)
* class [OoxmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
