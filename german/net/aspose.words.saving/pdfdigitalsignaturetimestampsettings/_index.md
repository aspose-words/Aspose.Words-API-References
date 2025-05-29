---
title: PdfDigitalSignatureTimestampSettings Class
linktitle: PdfDigitalSignatureTimestampSettings
articleTitle: PdfDigitalSignatureTimestampSettings
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.PdfDigitalSignatureTimestampSettings für die nahtlose Verwaltung digitaler Signatur-Zeitstempel. Verbessern Sie mühelos Ihre PDF-Sicherheit!
type: docs
weight: 6240
url: /de/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/
---
## PdfDigitalSignatureTimestampSettings class

Enthält Einstellungen für den Zeitstempel der digitalen Signatur.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit digitalen Signaturen](https://docs.aspose.com/words/net/working-with-digital-signatures/) Dokumentationsartikel.

```csharp
public class PdfDigitalSignatureTimestampSettings
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [PdfDigitalSignatureTimestampSettings](pdfdigitalsignaturetimestampsettings/#constructor)() | Initialisiert eine Instanz dieser Klasse. |
| [PdfDigitalSignatureTimestampSettings](pdfdigitalsignaturetimestampsettings/#constructor_1)(*string, string, string*) | Initialisiert eine Instanz dieser Klasse. |
| [PdfDigitalSignatureTimestampSettings](pdfdigitalsignaturetimestampsettings/#constructor_2)(*string, string, string, TimeSpan*) | Initialisiert eine Instanz dieser Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Password](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/password/) { get; set; } | Zeitstempel-Serverkennwort. |
| [ServerUrl](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/serverurl/) { get; set; } | Zeitstempel-Server-URL. |
| [Timeout](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/timeout/) { get; set; } | Timeout-Wert für den Zugriff auf den Zeitstempelserver. |
| [UserName](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/username/) { get; set; } | Zeitstempel-Serverbenutzername. |

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
