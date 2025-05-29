---
title: PdfDigitalSignatureTimestampSettings.ServerUrl
linktitle: ServerUrl
articleTitle: ServerUrl
second_title: Aspose.Words per .NET
description: Scopri la proprietà ServerUrl di PdfDigitalSignatureTimestampSettings per una marcatura temporale sicura. Garantisci l'integrità dei documenti con URL affidabili per il server di marcatura temporale.
type: docs
weight: 30
url: /it/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/serverurl/
---
## PdfDigitalSignatureTimestampSettings.ServerUrl property

URL del server di marcatura temporale.

```csharp
public string ServerUrl { get; set; }
```

## Osservazioni

Il valore predefinito è`null` . Se`null` , la firma digitale non verrà marcata oralmente.

## Esempi

Mostra come firmare digitalmente un documento PDF salvato e apporre una marca temporale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Creiamo una firma digitale e assegniamola al nostro oggetto SaveOptions per firmare il documento quando lo salviamo in PDF.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// Crea un timestamp verificato dall'autorità.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword");

// La durata predefinita del timestamp è 100 secondi.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// Possiamo impostare il periodo di timeout tramite il costruttore.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword", TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr", opzioni.Dettagli della firma digitale.Impostazioni timestamp.Url del server);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// Il metodo "Salva" applicherà la nostra firma al documento di output in questo momento.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### Guarda anche

* class [PdfDigitalSignatureTimestampSettings](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
