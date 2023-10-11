---
title: PdfDigitalSignatureDetails.TimestampSettings
second_title: Aspose.Words per .NET API Reference
description: PdfDigitalSignatureDetails proprietà. Ottiene o imposta le impostazioni del timestamp della firma digitale.
type: docs
weight: 70
url: /it/net/aspose.words.saving/pdfdigitalsignaturedetails/timestampsettings/
---
## PdfDigitalSignatureDetails.TimestampSettings property

Ottiene o imposta le impostazioni del timestamp della firma digitale.

```csharp
public PdfDigitalSignatureTimestampSettings TimestampSettings { get; set; }
```

### Osservazioni

Il valore predefinito è`nullo` e la firma digitale non verrà contrassegnata con data e ora. Quando questa proprietà è impostata su un valore valido[`PdfDigitalSignatureTimestampSettings`](../../pdfdigitalsignaturetimestampsettings/) object, , la firma digitale nel documento PDF verrà contrassegnata con data e ora.

### Esempi

Mostra come firmare digitalmente un documento PDF salvato e contrassegnarlo con data e ora.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Crea una firma digitale e assegnala al nostro oggetto SaveOptions per firmare il documento quando lo salviamo in PDF.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// Crea un timestamp verificato dall'autorità di timestamp.
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

* class [PdfDigitalSignatureTimestampSettings](../../pdfdigitalsignaturetimestampsettings/)
* class [PdfDigitalSignatureDetails](../)
* spazio dei nomi [Aspose.Words.Saving](../../pdfdigitalsignaturedetails/)
* assemblea [Aspose.Words](../../../)


