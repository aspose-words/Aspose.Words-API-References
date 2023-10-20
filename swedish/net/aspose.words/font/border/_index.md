---
title: Font.Border
linktitle: Border
articleTitle: Border
second_title: Aspose.Words för .NET
description: Font Border fast egendom. Returnerar enBorder objekt som anger kant för teckensnittet i C#.
type: docs
weight: 60
url: /sv/net/aspose.words/font/border/
---
## Font.Border property

Returnerar en[`Border`](../../border/) objekt som anger kant för teckensnittet.

```csharp
public Border Border { get; }
```

## Exempel

Visar hur man infogar en sträng omgiven av en kant i ett dokument.

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

* class [Border](../../border/)
* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
