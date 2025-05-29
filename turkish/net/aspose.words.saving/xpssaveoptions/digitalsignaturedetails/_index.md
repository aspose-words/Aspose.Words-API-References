---
title: XpsSaveOptions.DigitalSignatureDetails
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: .NET için Aspose.Words
description: Güvenli belge imzalama ve gelişmiş özgünlük için dijital imzaları kolayca yönetmek üzere XpsSaveOptions DigitalSignatureDetails özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/xpssaveoptions/digitalsignaturedetails/
---
## XpsSaveOptions.DigitalSignatureDetails property

Alır veya ayarlar[`DigitalSignatureDetails`](../../digitalsignaturedetails/) Bir belgeyi imzalamak için kullanılan nesne.

```csharp
public DigitalSignatureDetails DigitalSignatureDetails { get; set; }
```

## Örnekler

XPS belgesinin nasıl imzalanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
SignOptions options = new SignOptions();
options.SignTime = DateTime.Now;
options.Comments = "Some comments";

DigitalSignatureDetails digitalSignatureDetails = new DigitalSignatureDetails(certificateHolder, options);

XpsSaveOptions saveOptions = new XpsSaveOptions();
saveOptions.DigitalSignatureDetails = digitalSignatureDetails;

Assert.AreEqual(certificateHolder, digitalSignatureDetails.CertificateHolder);
Assert.AreEqual("Some comments", digitalSignatureDetails.SignOptions.Comments);

doc.Save(ArtifactsDir + "XpsSaveOptions.XpsDigitalSignature.docx", saveOptions);
```

### Ayrıca bakınız

* class [DigitalSignatureDetails](../../digitalsignaturedetails/)
* class [XpsSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
