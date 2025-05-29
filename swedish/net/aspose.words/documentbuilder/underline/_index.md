---
title: DocumentBuilder.Underline
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words för .NET
description: Upptäck DocumentBuilders egenskap Understrykning för att enkelt anpassa teckensnitt. Förbättra dina dokument med mångsidiga understrykningsalternativ för ett professionellt utseende.
type: docs
weight: 190
url: /sv/net/aspose.words/documentbuilder/underline/
---
## DocumentBuilder.Underline property

Hämtar/ställer in understrykningstyp för det aktuella teckensnittet.

```csharp
public Underline Underline { get; set; }
```

## Exempel

Visar hur man formaterar text som infogas av en dokumentbyggare.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Underline = Underline.Dash;
builder.Font.Color = Color.Blue;
builder.Font.Size = 32;

// Skaparen formaterar sitt aktuella stycke och all ny text som läggs till efteråt.
builder.Writeln("Large, blue, and underlined text.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertUnderline.docx");
```

### Se även

* enum [Underline](../../underline/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
