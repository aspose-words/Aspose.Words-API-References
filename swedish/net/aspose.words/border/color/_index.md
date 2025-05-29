---
title: Border.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words för .NET
description: Anpassa dina designer enkelt med egenskapen Kantfärg, så att du kan ställa in och ändra kantfärger för en fantastisk visuell effekt.
type: docs
weight: 10
url: /sv/net/aspose.words/border/color/
---
## Border.Color property

Hämtar eller ställer in kantfärgen.

```csharp
public Color Color { get; set; }
```

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
