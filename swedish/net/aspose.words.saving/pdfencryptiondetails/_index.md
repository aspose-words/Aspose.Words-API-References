---
title: PdfEncryptionDetails Class
linktitle: PdfEncryptionDetails
articleTitle: PdfEncryptionDetails
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.PdfEncryptionDetails för säker PDF-kryptering och anpassningsbara åtkomstbehörigheter, vilket säkerställer att dina dokument förblir skyddade.
type: docs
weight: 6250
url: /sv/net/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class

Innehåller information om kryptering och åtkomstbehörigheter för ett PDF-dokument.

För att lära dig mer, besök[Skydda eller kryptera ett dokument](https://docs.aspose.com/words/net/protect-or-encrypt-a-document/) dokumentationsartikel.

```csharp
public class PdfEncryptionDetails
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [PdfEncryptionDetails](pdfencryptiondetails/#constructor)(*string, string*) | Initierar en instans av denna klass. |
| [PdfEncryptionDetails](pdfencryptiondetails/#constructor_1)(*string, string, [PdfPermissions](../pdfpermissions/)*) | Initierar en instans av denna klass. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [OwnerPassword](../../aspose.words.saving/pdfencryptiondetails/ownerpassword/) { get; set; } | Anger ägarlösenordet för det krypterade PDF-dokumentet. |
| [Permissions](../../aspose.words.saving/pdfencryptiondetails/permissions/) { get; set; } | Anger de åtgärder som är tillåtna för en användare på ett krypterat PDF-dokument. Standardvärdet ärDisallowAll . |
| [UserPassword](../../aspose.words.saving/pdfencryptiondetails/userpassword/) { get; set; } | Anger användarlösenordet som krävs för att öppna det krypterade PDF-dokumentet. |

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
