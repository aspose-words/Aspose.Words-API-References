---
title: PdfDigitalSignatureTimestampSettings.ServerUrl
second_title: Aspose.Words für .NET-API-Referenz
description: PdfDigitalSignatureTimestampSettings eigendom. TimestampServerURL.
type: docs
weight: 30
url: /de/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/serverurl/
---
## PdfDigitalSignatureTimestampSettings.ServerUrl property

Timestamp-Server-URL.

```csharp
public string ServerUrl { get; set; }
```

### Bemerkungen

Der Standardwert ist null. Bei null wird die digitale Signatur nicht mit einem Zeitstempel versehen.

### Beispiele

Zeigt, wie ein gespeichertes PDF-Dokument digital signiert und mit einem Zeitstempel versehen wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

 // Erstellen Sie eine digitale Signatur und weisen Sie sie unserem SaveOptions-Objekt zu, um das Dokument zu signieren, wenn wir es als PDF speichern.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// Einen von der Behörde verifizierten Zeitstempel erstellen.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword");

// Die Standardlebensdauer des Zeitstempels beträgt 100 Sekunden.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// Wir können unsere Timeout-Periode über den Konstruktor festlegen.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword", TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr", options.DigitalSignatureDetails.TimestampSettings.ServerUrl);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// Die "Save"-Methode wendet zu diesem Zeitpunkt unsere Signatur auf das Ausgabedokument an.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### Siehe auch

* class [PdfDigitalSignatureTimestampSettings](../)
* namensraum [Aspose.Words.Saving](../../pdfdigitalsignaturetimestampsettings/)
* Montage [Aspose.Words](../../../)


