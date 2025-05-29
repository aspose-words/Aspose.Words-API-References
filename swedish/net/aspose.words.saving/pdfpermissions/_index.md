---
title: PdfPermissions Enum
linktitle: PdfPermissions
articleTitle: PdfPermissions
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.PdfPermissions enum för att kontrollera användaråtkomst till krypterade PDF-filer. Förbättra säkerheten och hantera dokumentåtgärder effektivt.
type: docs
weight: 6310
url: /sv/net/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enumeration

Anger de åtgärder som är tillåtna för en användare på ett krypterat PDF-dokument.

```csharp
[Flags]
public enum PdfPermissions
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| DisallowAll | `0` | Tillåter inte alla åtgärder på PDF-dokumentet. Detta är standardvärdet. |
| AllowAll | `FFFF` | Tillåter alla åtgärder på PDF-dokumentet. |
| ContentCopy | `10` | Kopiera eller på annat sätt extrahera text och grafik från dokumentet med andra åtgärder än de som kontrolleras avContentCopyForAccessibility . |
| ContentCopyForAccessibility | `200` | Extrahera text och grafik (för att underlätta tillgänglighet för användare med funktionsnedsättningar eller för andra ändamål). |
| ModifyContents | `8` | Ändra dokumentets innehåll med andra åtgärder än de som styrs av ModifyAnnotations ,FillIn ochDocumentAssembly . |
| ModifyAnnotations | `20` | Lägg till eller ändra textanteckningar, fyll i interaktiva formulärfält och, omModifyContents is även ställa in, skapa eller modifiera interaktiva formulärfält (inklusive signaturfält). |
| FillIn | `100` | Fyll i befintliga interaktiva formulärfält (inklusive signaturfält), även omModifyContents är klar. |
| DocumentAssembly | `400` | Sammanställ dokumentet (infoga, rotera eller ta bort sidor och skapa dokumentkonturobjekt eller miniatyrbilder), även omModifyContents är klart. |
| Printing | `4` | Skriv ut dokumentet (eventuellt inte med högsta kvalitetsnivå, beroende på om HighResolutionPrinting är också inställd). |
| HighResolutionPrinting | `804` | Skriv ut dokumentet till en representation från vilken en korrekt digital kopia av PDF-innehållet kan genereras, baserat på en implementeringsberoende algoritm. När denna flagga är tom (och Printing är inställt), ska utskrift begränsas till en lågnivårepresentation av utseendet, eventuellt av försämrad kvalitet. |

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

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
