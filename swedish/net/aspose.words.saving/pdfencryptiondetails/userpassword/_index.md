---
title: PdfEncryptionDetails.UserPassword
linktitle: UserPassword
articleTitle: UserPassword
second_title: Aspose.Words för .NET
description: PdfEncryptionDetails UserPassword fast egendom. Anger användarlösenordet som krävs för att öppna det krypterade PDFdokumentet i C#.
type: docs
weight: 40
url: /sv/net/aspose.words.saving/pdfencryptiondetails/userpassword/
---
## PdfEncryptionDetails.UserPassword property

Anger användarlösenordet som krävs för att öppna det krypterade PDF-dokumentet.

```csharp
public string UserPassword { get; set; }
```

## Anmärkningar

Användarlösenordet kommer att krävas för att öppna ett krypterat PDF-dokument för visning. Behörigheterna som anges i [`Permissions`](../permissions/) kommer att upprätthållas av läsarprogramvaran.

Användarlösenordet kan vara`null` eller tom sträng, i det här fallet kommer inget lösenord att krävas av användaren när öppnar PDF-dokumentet. Användarlösenordet kan inte vara detsamma som ägarlösenordet.

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

* class [PdfEncryptionDetails](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
