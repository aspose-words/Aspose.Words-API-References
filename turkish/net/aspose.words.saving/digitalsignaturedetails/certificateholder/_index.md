---
title: DigitalSignatureDetails.CertificateHolder
linktitle: CertificateHolder
articleTitle: CertificateHolder
second_title: .NET için Aspose.Words
description: Belgenizin imzalama sertifikasını zahmetsizce yönetmek için DigitalSignatureDetails CertificateHolder özelliğini keşfedin. Güvenliği artırın ve süreçleri kolaylaştırın!
type: docs
weight: 20
url: /tr/net/aspose.words.saving/digitalsignaturedetails/certificateholder/
---
## DigitalSignatureDetails.CertificateHolder property

Bir değeri alır veya ayarlar`CertificateHolder` Bir belgeyi imzalamak için kullanılan sertifikayı içeren nesne.

```csharp
public CertificateHolder CertificateHolder { get; set; }
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

* class [CertificateHolder](../../../aspose.words.digitalsignatures/certificateholder/)
* class [DigitalSignatureDetails](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
