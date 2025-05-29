---
title: PdfDigitalSignatureTimestampSettings.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words pour .NET
description: Sécurisez vos documents PDF avec PdfDigitalSignatureTimestampSettings. Gérez facilement les mots de passe des serveurs d'horodatage pour une protection et une conformité renforcées.
type: docs
weight: 20
url: /fr/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/password/
---
## PdfDigitalSignatureTimestampSettings.Password property

Mot de passe du serveur d'horodatage.

```csharp
public string Password { get; set; }
```

## Remarques

La valeur par défaut est`nul` .

## Exemples

Montre comment signer numériquement un document PDF enregistré et l'horodater.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Créez une signature numérique et attribuez-la à notre objet SaveOptions pour signer le document lorsque nous l'enregistrons au format PDF.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// Créer un horodatage vérifié par une autorité.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword");

// La durée de vie par défaut de l'horodatage est de 100 secondes.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// Nous pouvons définir notre délai d'expiration via le constructeur.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword", TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr", options.DigitalSignatureDetails.TimestampSettings.ServerUrl);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// La méthode « Enregistrer » appliquera notre signature au document de sortie à ce moment-là.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### Voir également

* class [PdfDigitalSignatureTimestampSettings](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
