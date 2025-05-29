---
title: PdfEncryptionDetails.OwnerPassword
linktitle: OwnerPassword
articleTitle: OwnerPassword
second_title: Aspose.Words för .NET
description: Upptäck hur OwnerPassword-egenskapen skyddar dina krypterade PDF-filer och garanterar endast behörig åtkomst. Skydda dina dokument utan ansträngning!
type: docs
weight: 20
url: /sv/net/aspose.words.saving/pdfencryptiondetails/ownerpassword/
---
## PdfEncryptionDetails.OwnerPassword property

Anger ägarlösenordet för det krypterade PDF-dokumentet.

```csharp
public string OwnerPassword { get; set; }
```

## Anmärkningar

Ägarlösenordet tillåter användaren att öppna ett krypterat PDF-dokument utan några åtkomstbegränsningar som anges i[`Permissions`](../permissions/).

Ägarlösenordet får inte vara detsamma som användarlösenordet.

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

* class [PdfEncryptionDetails](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
