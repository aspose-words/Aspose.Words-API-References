---
title: Border.LineWidth
linktitle: LineWidth
articleTitle: LineWidth
second_title: Aspose.Words för .NET
description: Justera egenskapen Border LineWidth för att anpassa kanttjockleken i punkter, vilket förbättrar designens precision och visuella attraktionskraft.
type: docs
weight: 50
url: /sv/net/aspose.words/border/linewidth/
---
## Border.LineWidth property

Hämtar eller ställer in kantbredden i punkter.

```csharp
public double LineWidth { get; set; }
```

## Anmärkningar

Om du ställer in linjebredden större än noll när linjestilen är ingen, ändras linjestilen is automatiskt till en enda rad.

## Exempel

Visar hur man infogar en sträng omgiven av en kantlinje i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

### Se även

* class [Border](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
