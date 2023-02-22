---
title: PdfSaveOptions.DigitalSignatureDetails
second_title: Référence de l'API Aspose.Words pour .NET
description: PdfSaveOptions propriété. Obtient ou définit les détails de signature du document PDF de sortie.
type: docs
weight: 60
url: /fr/net/aspose.words.saving/pdfsaveoptions/digitalsignaturedetails/
---
## PdfSaveOptions.DigitalSignatureDetails property

Obtient ou définit les détails de signature du document PDF de sortie.

```csharp
public PdfDigitalSignatureDetails DigitalSignatureDetails { get; set; }
```

### Remarques

La valeur par défaut est nulle et le document de sortie ne sera pas signé. Lorsque cette propriété est définie sur un[`PdfDigitalSignatureDetails`](../../pdfdigitalsignaturedetails/) object, , le document PDF de sortie sera signé numériquement.

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

* class [PdfDigitalSignatureDetails](../../pdfdigitalsignaturedetails/)
* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../pdfsaveoptions/)
* Assemblée [Aspose.Words](../../../)


