---
title: PdfDigitalSignatureHashAlgorithm Enum
linktitle: PdfDigitalSignatureHashAlgorithm
articleTitle: PdfDigitalSignatureHashAlgorithm
second_title: Aspose.Words pour .NET
description: Explorez l'énumération Aspose.Words PdfDigitalSignatureHashAlgorithm, définissant des algorithmes de hachage numérique pour des signatures numériques sécurisées dans vos documents.
type: docs
weight: 6230
url: /fr/net/aspose.words.saving/pdfdigitalsignaturehashalgorithm/
---
## PdfDigitalSignatureHashAlgorithm enumeration

Spécifie un algorithme de hachage numérique utilisé par une signature numérique.

```csharp
public enum PdfDigitalSignatureHashAlgorithm
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Sha256 | `0` | Algorithme de hachage SHA-256. |
| Sha384 | `1` | Algorithme de hachage SHA-384. |
| Sha512 | `2` | Algorithme de hachage SHA-512. |
| RipeMD160 | `3` | Algorithme de hachage RIPEMD-160. |

## Exemples

Montre comment signer un document PDF généré.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Contents of signed PDF.");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Configurez l'objet « DigitalSignatureDetails » de l'objet « SaveOptions » pour
// signer numériquement le document tel que nous le rendons avec la méthode « Enregistrer ».
DateTime signingTime = new DateTime(2015, 7, 20);
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.RipeMD160;

Assert.AreEqual("Test Signing", options.DigitalSignatureDetails.Reason);
Assert.AreEqual("My Office", options.DigitalSignatureDetails.Location);
Assert.AreEqual(signingTime, options.DigitalSignatureDetails.SignatureDate.ToLocalTime());
Assert.AreEqual(certificateHolder, options.DigitalSignatureDetails.CertificateHolder);

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
