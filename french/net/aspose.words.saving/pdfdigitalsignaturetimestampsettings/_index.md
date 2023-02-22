---
title: Class PdfDigitalSignatureTimestampSettings
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.PdfDigitalSignatureTimestampSettings classe. Contient les paramètres de lhorodatage de la signature numérique.
type: docs
weight: 5170
url: /fr/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/
---
## PdfDigitalSignatureTimestampSettings class

Contient les paramètres de l'horodatage de la signature numérique.

```csharp
public class PdfDigitalSignatureTimestampSettings
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [PdfDigitalSignatureTimestampSettings](pdfdigitalsignaturetimestampsettings/#constructor)() | Initialise une instance de cette classe. |
| [PdfDigitalSignatureTimestampSettings](pdfdigitalsignaturetimestampsettings/#constructor_1)(string, string, string) | Initialise une instance de cette classe. |
| [PdfDigitalSignatureTimestampSettings](pdfdigitalsignaturetimestampsettings/#constructor_2)(string, string, string, TimeSpan) | Initialise une instance de cette classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [Password](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/password/) { get; set; } | Mot de passe du serveur d'horodatage. |
| [ServerUrl](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/serverurl/) { get; set; } | URL du serveur d'horodatage. |
| [Timeout](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/timeout/) { get; set; } | Valeur du délai d'attente pour accéder au serveur d'horodatage. |
| [UserName](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/username/) { get; set; } | Nom d'utilisateur du serveur d'horodatage. |

### Exemples

Montre comment signer numériquement un document PDF enregistré et l'horodater.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// Crée un objet "PdfSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

 // Créez une signature numérique et attribuez-la à notre objet SaveOptions pour signer le document lorsque nous l'enregistrons au format PDF.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// Crée un horodatage vérifié par l'autorité.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword");

// La durée de vie par défaut de l'horodatage est de 100 secondes.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// Nous pouvons définir notre délai d'attente via le constructeur.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword", TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr", options.DigitalSignatureDetails.TimestampSettings.ServerUrl);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// La méthode "Save" appliquera notre signature au document de sortie à ce moment.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)


