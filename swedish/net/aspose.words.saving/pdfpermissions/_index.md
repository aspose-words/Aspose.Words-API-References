---
title: Enum PdfPermissions
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Saving.PdfPermissions uppräkning. Anger de operationer som är tillåtna för en användare på ett krypterat PDFdokument.
type: docs
weight: 5230
url: /sv/net/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enumeration

Anger de operationer som är tillåtna för en användare på ett krypterat PDF-dokument.

```csharp
[Flags]
public enum PdfPermissions
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| DisallowAll | `0` | Tillåter inte alla operationer på PDF-dokumentet. Detta är standardvärdet. |
| AllowAll | `FFFF` | Tillåter alla operationer på PDF-dokumentet. |
| ContentCopy | `10` | Kopiera eller på annat sätt extrahera text och grafik från dokumentet genom andra operationer än de som kontrolleras avContentCopyForAccessibility . |
| ContentCopyForAccessibility | `200` | Extrahera text och grafik (till stöd för tillgänglighet för användare med funktionshinder eller för andra ändamål). |
| ModifyContents | `8` | Ändra innehållet i dokumentet genom andra operationer än de som kontrolleras av ModifyAnnotations ,FillIn , ochDocumentAssembly . |
| ModifyAnnotations | `20` | Lägg till eller ändra textkommentarer, fyll i interaktiva formulärfält och, omModifyContents is ställer också in, skapar eller ändrar interaktiva formulärfält (inklusive signaturfält). |
| FillIn | `100` | Fyll i befintliga interaktiva formulärfält (inklusive signaturfält), även omModifyContents är klar. |
| DocumentAssembly | `400` | Sätt ihop dokumentet (infoga, rotera eller ta bort sidor och skapa dokumentkonturobjekt eller thumbnail bilder), även omModifyContents är klar. |
| Printing | `4` | Skriv ut dokumentet (möjligen inte på högsta kvalitetsnivå, beroende på om HighResolutionPrintingär också inställd). |
| HighResolutionPrinting | `804` | Skriv ut dokumentet till en representation från vilken en trogen digital kopia av PDF-innehållet kan genereras, baserat på en implementeringsberoende algoritm. När denna flagga är klar (and Printing är inställd), ska utskriften begränsas till en lågnivårepresentation av utseendet, möjligen av försämrad kvalitet. |

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

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)


