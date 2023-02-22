---
title: PdfEncryptionDetails.PdfEncryptionDetails
second_title: Aspose.Words för .NET API Referens
description: PdfEncryptionDetails byggare. Initierar en instans av denna klass.
type: docs
weight: 10
url: /sv/net/aspose.words.saving/pdfencryptiondetails/pdfencryptiondetails/
---
## PdfEncryptionDetails constructor

Initierar en instans av denna klass.

```csharp
public PdfEncryptionDetails(string userPassword, string ownerPassword)
```

### Exempel

Visar hur man ställer in behörigheter för ett sparat PDF-dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty);

// Börja med att inte tillåta alla behörigheter.
encryptionDetails.Permissions = PdfPermissions.DisallowAll;

// Utöka behörigheter för att tillåta redigering av kommentarer.
encryptionDetails.Permissions = PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly;

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Aktivera kryptering via egenskapen "EncryptionDetails".
saveOptions.EncryptionDetails = encryptionDetails;

// När vi öppnar det här dokumentet måste vi ange lösenordet innan vi kan komma åt dess innehåll.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### Se även

* class [PdfEncryptionDetails](../)
* namnutrymme [Aspose.Words.Saving](../../pdfencryptiondetails/)
* hopsättning [Aspose.Words](../../../)


