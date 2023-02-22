---
title: PdfDigitalSignatureTimestampSettings.PdfDigitalSignatureTimestampSettings
second_title: Aspose.Words per .NET API Reference
description: PdfDigitalSignatureTimestampSettings costruttore. Inizializza unistanza di questa classe.
type: docs
weight: 10
url: /it/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/pdfdigitalsignaturetimestampsettings/
---
## PdfDigitalSignatureTimestampSettings() {#constructor}

Inizializza un'istanza di questa classe.

```csharp
public PdfDigitalSignatureTimestampSettings()
```

### Esempi

Mostra come firmare digitalmente un documento PDF salvato e contrassegnarlo con un timestamp.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

 // Crea una firma digitale e assegnala al nostro oggetto SaveOptions per firmare il documento quando lo salviamo in PDF.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// Crea un timestamp con autorizzazione verificata.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword");

// La durata predefinita del timestamp è 100 secondi.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// Possiamo impostare il nostro periodo di timeout tramite il costruttore.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword", TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr", options.DigitalSignatureDetails.TimestampSettings.ServerUrl);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// Il metodo "Salva" applicherà la nostra firma al documento di output in questo momento.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### Guarda anche

* class [PdfDigitalSignatureTimestampSettings](../)
* spazio dei nomi [Aspose.Words.Saving](../../pdfdigitalsignaturetimestampsettings/)
* assemblea [Aspose.Words](../../../)

---

## PdfDigitalSignatureTimestampSettings(string, string, string) {#constructor_1}

Inizializza un'istanza di questa classe.

```csharp
public PdfDigitalSignatureTimestampSettings(string serverUrl, string userName, string password)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| serverUrl | String | URL del server timestamp. |
| userName | String | Nome utente del server timestamp. |
| password | String | Password del server timestamp. |

### Esempi

Mostra come firmare digitalmente un documento PDF salvato e contrassegnarlo con un timestamp.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

 // Crea una firma digitale e assegnala al nostro oggetto SaveOptions per firmare il documento quando lo salviamo in PDF.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// Crea un timestamp con autorizzazione verificata.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword");

// La durata predefinita del timestamp è 100 secondi.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// Possiamo impostare il nostro periodo di timeout tramite il costruttore.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword", TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr", options.DigitalSignatureDetails.TimestampSettings.ServerUrl);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// Il metodo "Salva" applicherà la nostra firma al documento di output in questo momento.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### Guarda anche

* class [PdfDigitalSignatureTimestampSettings](../)
* spazio dei nomi [Aspose.Words.Saving](../../pdfdigitalsignaturetimestampsettings/)
* assemblea [Aspose.Words](../../../)

---

## PdfDigitalSignatureTimestampSettings(string, string, string, TimeSpan) {#constructor_2}

Inizializza un'istanza di questa classe.

```csharp
public PdfDigitalSignatureTimestampSettings(string serverUrl, string userName, string password, 
    TimeSpan timeout)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| serverUrl | String | URL del server timestamp. |
| userName | String | Nome utente del server timestamp. |
| password | String | Password del server timestamp. |
| timeout | TimeSpan | Valore di timeout per l'accesso al server timestamp. |

### Esempi

Mostra come firmare digitalmente un documento PDF salvato e contrassegnarlo con un timestamp.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

 // Crea una firma digitale e assegnala al nostro oggetto SaveOptions per firmare il documento quando lo salviamo in PDF.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// Crea un timestamp con autorizzazione verificata.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword");

// La durata predefinita del timestamp è 100 secondi.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// Possiamo impostare il nostro periodo di timeout tramite il costruttore.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword", TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr", options.DigitalSignatureDetails.TimestampSettings.ServerUrl);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// Il metodo "Salva" applicherà la nostra firma al documento di output in questo momento.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### Guarda anche

* class [PdfDigitalSignatureTimestampSettings](../)
* spazio dei nomi [Aspose.Words.Saving](../../pdfdigitalsignaturetimestampsettings/)
* assemblea [Aspose.Words](../../../)


