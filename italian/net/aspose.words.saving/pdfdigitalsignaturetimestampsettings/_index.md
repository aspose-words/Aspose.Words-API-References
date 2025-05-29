---
title: PdfDigitalSignatureTimestampSettings Class
linktitle: PdfDigitalSignatureTimestampSettings
articleTitle: PdfDigitalSignatureTimestampSettings
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.PdfDigitalSignatureTimestampSettings per una gestione semplificata della marca temporale delle firme digitali. Migliora la sicurezza dei tuoi PDF senza sforzo!
type: docs
weight: 6240
url: /it/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/
---
## PdfDigitalSignatureTimestampSettings class

Contiene le impostazioni del timestamp della firma digitale.

Per saperne di più, visita il[Lavorare con le firme digitali](https://docs.aspose.com/words/net/working-with-digital-signatures/) articolo di documentazione.

```csharp
public class PdfDigitalSignatureTimestampSettings
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [PdfDigitalSignatureTimestampSettings](pdfdigitalsignaturetimestampsettings/#constructor)() | Inizializza un'istanza di questa classe. |
| [PdfDigitalSignatureTimestampSettings](pdfdigitalsignaturetimestampsettings/#constructor_1)(*string, string, string*) | Inizializza un'istanza di questa classe. |
| [PdfDigitalSignatureTimestampSettings](pdfdigitalsignaturetimestampsettings/#constructor_2)(*string, string, string, TimeSpan*) | Inizializza un'istanza di questa classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Password](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/password/) { get; set; } | Password del server di marcatura temporale. |
| [ServerUrl](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/serverurl/) { get; set; } | URL del server di marcatura temporale. |
| [Timeout](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/timeout/) { get; set; } | Valore di timeout per l'accesso al server di marcatura temporale. |
| [UserName](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/username/) { get; set; } | Nome utente del server di marcatura temporale. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
