---
title: PdfDigitalSignatureTimestampSettings
second_title: Référence de l'API Aspose.Words pour .NET
description: Initialise une instance de cette classe.
type: docs
weight: 10
url: /fr/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/pdfdigitalsignaturetimestampsettings/
---
## PdfDigitalSignatureTimestampSettings() {#constructor}

Initialise une instance de cette classe.

```csharp
public PdfDigitalSignatureTimestampSettings()
```

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

* class [PdfDigitalSignatureTimestampSettings](../../pdfdigitalsignaturetimestampsettings)
* espace de noms [Aspose.Words.Saving](../../pdfdigitalsignaturetimestampsettings)
* Assemblée [Aspose.Words](../../../)

---

## PdfDigitalSignatureTimestampSettings(string, string, string) {#constructor_1}

Initialise une instance de cette classe.

```csharp
public PdfDigitalSignatureTimestampSettings(string serverUrl, string userName, string password)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| serverUrl | String | URL du serveur d'horodatage. |
| userName | String | Nom d'utilisateur du serveur d'horodatage. |
| password | String | Mot de passe du serveur d'horodatage. |

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

* class [PdfDigitalSignatureTimestampSettings](../../pdfdigitalsignaturetimestampsettings)
* espace de noms [Aspose.Words.Saving](../../pdfdigitalsignaturetimestampsettings)
* Assemblée [Aspose.Words](../../../)

---

## PdfDigitalSignatureTimestampSettings(string, string, string, TimeSpan) {#constructor_2}

Initialise une instance de cette classe.

```csharp
public PdfDigitalSignatureTimestampSettings(string serverUrl, string userName, string password, 
    TimeSpan timeout)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| serverUrl | String | URL du serveur d'horodatage. |
| userName | String | Nom d'utilisateur du serveur d'horodatage. |
| password | String | Mot de passe du serveur d'horodatage. |
| timeout | TimeSpan | Valeur du délai d'attente pour accéder au serveur d'horodatage. |

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

* class [PdfDigitalSignatureTimestampSettings](../../pdfdigitalsignaturetimestampsettings)
* espace de noms [Aspose.Words.Saving](../../pdfdigitalsignaturetimestampsettings)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
