---
title: PdfDigitalSignatureTimestampSettings
linktitle: PdfDigitalSignatureTimestampSettings
articleTitle: PdfDigitalSignatureTimestampSettings
second_title: Aspose.Words för .NET
description: Upptäck konstruktorn PdfDigitalSignatureTimestampSettings för att enkelt initiera inställningar för digitala signaturer för förbättrad dokumentsäkerhet och efterlevnad.
type: docs
weight: 10
url: /sv/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/pdfdigitalsignaturetimestampsettings/
---
## PdfDigitalSignatureTimestampSettings() {#constructor}

Initierar en instans av denna klass.

```csharp
public PdfDigitalSignatureTimestampSettings()
```

## Exempel

Visar hur man signerar ett sparat PDF-dokument digitalt och tidsstämplar det.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Skapa en digital signatur och tilldela den till vårt SaveOptions-objekt för att signera dokumentet när vi sparar det som PDF.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// Skapa en tidsstämpel som verifierats av en tidsstämpel, auktoritetsverifierad.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "Mitt lösenord");

// Standardlivslängden för tidsstämpeln är 100 sekunder.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// Vi kan ställa in vår timeout-period via konstruktorn.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword", TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr", options.DigitalSignatureDetails.TimestampSettings.ServerUrl);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// Metoden "Spara" kommer att tillämpa vår signatur på utdatadokumentet vid denna tidpunkt.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### Se även

* class [PdfDigitalSignatureTimestampSettings](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)

---

## PdfDigitalSignatureTimestampSettings(*string, string, string*) {#constructor_1}

Initierar en instans av denna klass.

```csharp
public PdfDigitalSignatureTimestampSettings(string serverUrl, string userName, string password)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| serverUrl | String | Tidsstämpelserverns URL. |
| userName | String | Användarnamn för tidsstämpelserver. |
| password | String | Lösenord för tidsstämpelserver. |

## Exempel

Visar hur man signerar ett sparat PDF-dokument digitalt och tidsstämplar det.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Skapa en digital signatur och tilldela den till vårt SaveOptions-objekt för att signera dokumentet när vi sparar det som PDF.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// Skapa en tidsstämpel som verifierats av en tidsstämpel, auktoritetsverifierad.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "Mitt lösenord");

// Standardlivslängden för tidsstämpeln är 100 sekunder.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// Vi kan ställa in vår timeout-period via konstruktorn.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword", TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr", options.DigitalSignatureDetails.TimestampSettings.ServerUrl);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// Metoden "Spara" kommer att tillämpa vår signatur på utdatadokumentet vid denna tidpunkt.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### Se även

* class [PdfDigitalSignatureTimestampSettings](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)

---

## PdfDigitalSignatureTimestampSettings(*string, string, string, TimeSpan*) {#constructor_2}

Initierar en instans av denna klass.

```csharp
public PdfDigitalSignatureTimestampSettings(string serverUrl, string userName, string password, 
    TimeSpan timeout)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| serverUrl | String | Tidsstämpelserverns URL. |
| userName | String | Användarnamn för tidsstämpelserver. |
| password | String | Lösenord för tidsstämpelserver. |
| timeout | TimeSpan | Timeout-värde för åtkomst till tidsstämpelservern. |

## Exempel

Visar hur man signerar ett sparat PDF-dokument digitalt och tidsstämplar det.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Skapa en digital signatur och tilldela den till vårt SaveOptions-objekt för att signera dokumentet när vi sparar det som PDF.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// Skapa en tidsstämpel som verifierats av en tidsstämpel, auktoritetsverifierad.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "Mitt lösenord");

// Standardlivslängden för tidsstämpeln är 100 sekunder.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// Vi kan ställa in vår timeout-period via konstruktorn.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword", TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr", options.DigitalSignatureDetails.TimestampSettings.ServerUrl);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// Metoden "Spara" kommer att tillämpa vår signatur på utdatadokumentet vid denna tidpunkt.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### Se även

* class [PdfDigitalSignatureTimestampSettings](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
