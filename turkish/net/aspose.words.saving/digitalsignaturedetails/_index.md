---
title: DigitalSignatureDetails Class
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: .NET için Aspose.Words
description: Sorunsuz dijital belge imzalama için Aspose.Words.Saving.DigitalSignatureDetails sınıfını keşfedin. Güvenliği ve özgünlüğü zahmetsizce artırın!
type: docs
weight: 5640
url: /tr/net/aspose.words.saving/digitalsignaturedetails/
---
## DigitalSignatureDetails class

Bir belgeyi dijital imzayla imzalamaya ilişkin ayrıntıları içerir.

```csharp
public class DigitalSignatureDetails
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [DigitalSignatureDetails](digitalsignaturedetails/)(*[CertificateHolder](../../aspose.words.digitalsignatures/certificateholder/), [SignOptions](../../aspose.words.digitalsignatures/signoptions/)*) | Yeni bir örneğini başlatır`DigitalSignatureDetails` sınıf. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CertificateHolder](../../aspose.words.saving/digitalsignaturedetails/certificateholder/) { get; set; } | Bir değeri alır veya ayarlar[`CertificateHolder`](./certificateholder/) Bir belgeyi imzalamak için kullanılan sertifikayı içeren nesne. |
| [SignOptions](../../aspose.words.saving/digitalsignaturedetails/signoptions/) { get; set; } | Bir değeri alır veya ayarlar[`SignOptions`](./signoptions/) Bir belgeyi imzalamak için kullanılan nesne. |

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
