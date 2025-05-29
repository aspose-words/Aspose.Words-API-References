---
title: PdfDigitalSignatureDetails.TimestampSettings
linktitle: TimestampSettings
articleTitle: TimestampSettings
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „PdfDigitalSignatureDetails TimestampSettings“, um Zeitstempel digitaler Signaturen einfach zu verwalten und so die Dokumentensicherheit und -konformität zu verbessern.
type: docs
weight: 70
url: /de/net/aspose.words.saving/pdfdigitalsignaturedetails/timestampsettings/
---
## PdfDigitalSignatureDetails.TimestampSettings property

Ruft die Zeitstempeleinstellungen für die digitale Signatur ab oder legt sie fest.

```csharp
public PdfDigitalSignatureTimestampSettings TimestampSettings { get; set; }
```

## Bemerkungen

Der Standardwert ist`null` und die digitale Signatur wird nicht mit einem Zeitstempel versehen. Wenn diese Eigenschaft auf einen gültigen Wert gesetzt ist[`PdfDigitalSignatureTimestampSettings`](../../pdfdigitalsignaturetimestampsettings/) object, , dann wird die digitale Signatur im PDF-Dokument mit einem Zeitstempel versehen.

## Beispiele

Zeigt, wie Sie ein gespeichertes PDF-Dokument digital signieren und mit einem Zeitstempel versehen.

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

// Erstellen Sie einen von einer Zeitstempelbehörde verifizierten Zeitstempel.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", „JohnDoe“, „MyPassword“);

// Die Standardlebensdauer des Zeitstempels beträgt 100 Sekunden.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// Wir können unsere Timeout-Periode über den Konstruktor festlegen.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", „JohnDoe“, „MyPassword“, TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr", Optionen.DigitalSignatureDetails.TimestampSettings.ServerUrl);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// Die Methode „Speichern“ wendet unsere Signatur jetzt auf das Ausgabedokument an.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### Siehe auch

* class [PdfDigitalSignatureTimestampSettings](../../pdfdigitalsignaturetimestampsettings/)
* class [PdfDigitalSignatureDetails](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
