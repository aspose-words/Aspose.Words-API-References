---
title: DigitalSignatureDetails Class
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Saving.DigitalSignatureDetails pour une signature numérique fluide de vos documents. Améliorez la sécurité et l'authenticité sans effort !
type: docs
weight: 5640
url: /fr/net/aspose.words.saving/digitalsignaturedetails/
---
## DigitalSignatureDetails class

Contient des détails pour signer un document avec une signature numérique.

```csharp
public class DigitalSignatureDetails
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [DigitalSignatureDetails](digitalsignaturedetails/)(*[CertificateHolder](../../aspose.words.digitalsignatures/certificateholder/), [SignOptions](../../aspose.words.digitalsignatures/signoptions/)*) | Initialise une nouvelle instance de`DigitalSignatureDetails` classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [CertificateHolder](../../aspose.words.saving/digitalsignaturedetails/certificateholder/) { get; set; } | Obtient ou définit un[`CertificateHolder`](./certificateholder/) objet qui contient le certificat utilisé pour signer un document. |
| [SignOptions](../../aspose.words.saving/digitalsignaturedetails/signoptions/) { get; set; } | Obtient ou définit un[`SignOptions`](./signoptions/) objet utilisé pour signer un document. |

## Exemples

Montre comment signer un document OOXML.

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

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
