---
title: DigitalSignatureDetails.SignOptions
linktitle: SignOptions
articleTitle: SignOptions
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété DigitalSignatureDetails SignOptions améliore la sécurité des documents en gérant facilement les options de signature pour des signatures numériques transparentes.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/digitalsignaturedetails/signoptions/
---
## DigitalSignatureDetails.SignOptions property

Obtient ou définit un`SignOptions` objet utilisé pour signer un document.

```csharp
public SignOptions SignOptions { get; set; }
```

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

* class [SignOptions](../../../aspose.words.digitalsignatures/signoptions/)
* class [DigitalSignatureDetails](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
