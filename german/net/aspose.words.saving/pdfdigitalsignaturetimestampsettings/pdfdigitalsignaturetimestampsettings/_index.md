---
title: PdfDigitalSignatureTimestampSettings
second_title: Aspose.Words für .NET-API-Referenz
description: Initialisiert eine Instanz dieser Klasse.
type: docs
weight: 10
url: /de/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/pdfdigitalsignaturetimestampsettings/
---
## PdfDigitalSignatureTimestampSettings() {#constructor}

Initialisiert eine Instanz dieser Klasse.

```csharp
public PdfDigitalSignatureTimestampSettings()
```

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

---

## PdfDigitalSignatureTimestampSettings(string, string, string) {#constructor_1}

Initialisiert eine Instanz dieser Klasse.

```csharp
public PdfDigitalSignatureTimestampSettings(string serverUrl, string userName, string password)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| serverUrl | String | Zeitstempel-Server-URL. |
| userName | String | Benutzername des Timestamp-Servers. |
| password | String | Kennwort des Timestamp-Servers. |

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

---

## PdfDigitalSignatureTimestampSettings(string, string, string, TimeSpan) {#constructor_2}

Initialisiert eine Instanz dieser Klasse.

```csharp
public PdfDigitalSignatureTimestampSettings(string serverUrl, string userName, string password, 
    TimeSpan timeout)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| serverUrl | String | Zeitstempel-Server-URL. |
| userName | String | Benutzername des Timestamp-Servers. |
| password | String | Kennwort des Timestamp-Servers. |
| timeout | TimeSpan | Zeitüberschreitungswert für den Zugriff auf den Zeitstempelserver. |

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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
