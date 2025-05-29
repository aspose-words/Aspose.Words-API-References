---
title: PdfDigitalSignatureDetails.HashAlgorithm
linktitle: HashAlgorithm
articleTitle: HashAlgorithm
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PdfDigitalSignatureDetails HashAlgorithm : gérez et personnalisez efficacement vos algorithmes de hachage pour une sécurité numérique renforcée.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/pdfdigitalsignaturedetails/hashalgorithm/
---
## PdfDigitalSignatureDetails.HashAlgorithm property

Obtient ou définit l'algorithme de hachage.

```csharp
public PdfDigitalSignatureHashAlgorithm HashAlgorithm { get; set; }
```

## Remarques

La valeur par défaut est l'algorithme SHA-256.

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

* enum [PdfDigitalSignatureHashAlgorithm](../../pdfdigitalsignaturehashalgorithm/)
* class [PdfDigitalSignatureDetails](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
