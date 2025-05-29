---
title: Font.Kerning
linktitle: Kerning
articleTitle: Kerning
second_title: Aspose.Words för .NET
description: Upptäck funktionen för teckensnittskärning, kontrollera när kärningen börjar för optimal textskärpa och design. Förbättra din typografi med precision!
type: docs
weight: 180
url: /sv/net/aspose.words/font/kerning/
---
## Font.Kerning property

Hämtar eller ställer in teckenstorleken där kerning börjar.

```csharp
public double Kerning { get; set; }
```

## Exempel

Visar hur man anger teckenstorleken då kerning börjar gälla.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial Black";

// Ange teckenstorlek för verktyget och den minsta storleken då kerning ska träda i kraft.
// Teckenstorleken understiger kerningtröskeln, så körningen nedan kommer inte att ha kerning.
builder.Font.Size = 18;
builder.Font.Kerning = 24;

builder.Writeln("TALLY. (Kerning not applied)");

// Ställ in kerningtröskeln så att byggerens nuvarande teckenstorlek är över den.
// All text vi lägger till från denna punkt kommer att få kerning tillämpad. Mellanrummen mellan tecknen
// kommer att justeras, vilket normalt resulterar i en något mer estetiskt tilltalande textförlopp.
builder.Font.Kerning = 12;

builder.Writeln("TALLY. (Kerning applied)");

doc.Save(ArtifactsDir + "Font.Kerning.docx");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
