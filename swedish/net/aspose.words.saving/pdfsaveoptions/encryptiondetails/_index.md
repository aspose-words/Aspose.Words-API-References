---
title: PdfSaveOptions.EncryptionDetails
linktitle: EncryptionDetails
articleTitle: EncryptionDetails
second_title: Aspose.Words för .NET
description: Upptäck PdfSaveOptions egenskap EncryptionDetails för att enkelt konfigurera PDF-krypteringsinställningar, vilket säkerställer att dina dokument förblir säkra och skyddade.
type: docs
weight: 130
url: /sv/net/aspose.words.saving/pdfsaveoptions/encryptiondetails/
---
## PdfSaveOptions.EncryptionDetails property

Hämtar eller anger detaljerna för kryptering av PDF-dokumentet.

```csharp
public PdfEncryptionDetails EncryptionDetails { get; set; }
```

## Anmärkningar

Standardvärdet är`null` och utdatadokumentet kommer inte att krypteras. När den här egenskapen är inställd på ett giltigt[`PdfEncryptionDetails`](../../pdfencryptiondetails/)objekt, så kommer det utgående PDF-dokumentet att krypteras.

AES-128-krypteringsalgoritmen används vid sparning till PDF 1.7-baserad kompatibilitet (inklusive PDF/UA-1). AES-256-krypteringsalgoritmen används vid sparning till PDF 2.0-baserad kompatibilitet.

Kryptering är förbjuden enligt PDF/A-standarden. Det här alternativet ignoreras när du sparar till PDF/A.

ContentCopyForAccessibility Åtkomst krävs av PDF/UA compliance om utdatadokumentet är krypterat. Denna behörighet används automatiskt när du sparar till PDF/UA.

ContentCopyForAccessibility behörigheten är föråldrad i PDF 2.0-format. Denna behörighet ignoreras när du sparar till PDF 2.0.

## Exempel

Visar hur man anger behörigheter för ett sparat PDF-dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Utöka behörigheter för att tillåta redigering av anteckningar.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Aktivera kryptering via egenskapen "EncryptionDetails".
saveOptions.EncryptionDetails = encryptionDetails;

// När vi öppnar det här dokumentet måste vi ange lösenordet innan vi får åtkomst till dess innehåll.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### Se även

* class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
