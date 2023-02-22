---
title: Enum PdfDigitalSignatureHashAlgorithm
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.PdfDigitalSignatureHashAlgorithm énumération. Spécifie un algorithme de hachage numérique utilisé par une signature numérique.
type: docs
weight: 5160
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

### Exemples

Montre comment signer un document PDF généré.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Contents of signed PDF.");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Crée un objet "PdfSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Configurez l'objet "DigitalSignatureDetails" de l'objet "SaveOptions" pour
// signe numériquement le document tel que nous le rendons avec la méthode "Save".
DateTime signingTime = DateTime.Now;
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.Sha256;

Assert.AreEqual("Test Signing", options.DigitalSignatureDetails.Reason);
Assert.AreEqual("My Office", options.DigitalSignatureDetails.Location);
Assert.AreEqual(signingTime.ToUniversalTime(), options.DigitalSignatureDetails.SignatureDate.ToUniversalTime());

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)


