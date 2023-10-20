---
title: PdfSaveOptions.EncryptionDetails
linktitle: EncryptionDetails
articleTitle: EncryptionDetails
second_title: Aspose.Words för .NET
description: PdfSaveOptions EncryptionDetails fast egendom. Hämtar eller ställer in detaljerna för kryptering av PDFdokumentet i C#.
type: docs
weight: 130
url: /sv/net/aspose.words.saving/pdfsaveoptions/encryptiondetails/
---
## PdfSaveOptions.EncryptionDetails property

Hämtar eller ställer in detaljerna för kryptering av PDF-dokumentet.

```csharp
public PdfEncryptionDetails EncryptionDetails { get; set; }
```

## Anmärkningar

Standardvärdet är`null` och utdatadokumentet kommer inte att krypteras. När denna egenskap är inställd på en giltig[`PdfEncryptionDetails`](../../pdfencryptiondetails/) object, då krypteras PDF-dokumentet.

AES-128-krypteringsalgoritm används när du sparar till PDF 1.7-baserad överensstämmelse (inklusive PDF/UA-1). AES-256-krypteringsalgoritm används när du sparar till PDF 2.0-baserad överensstämmelse.

Kryptering är förbjuden av PDF/A-kompatibilitet. Detta alternativ kommer att ignoreras när du sparar till PDF/A.

ContentCopyForAccessibility tillstånd krävs av PDF/UA compliance om utdatadokumentet är krypterat. Denna behörighet används automatiskt när du sparar till PDF/UA.

ContentCopyForAccessibility behörigheten är föråldrad i PDF 2.0-format. Denna behörighet kommer att ignoreras när du sparar till PDF 2.0.

## Exempel

Visar hur man ställer in behörigheter för ett sparat PDF-dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Utöka behörigheter för att tillåta redigering av kommentarer.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Aktivera kryptering via egenskapen "EncryptionDetails".
saveOptions.EncryptionDetails = encryptionDetails;

// När vi öppnar det här dokumentet måste vi ange lösenordet innan vi kan komma åt dess innehåll.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### Se även

* class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
