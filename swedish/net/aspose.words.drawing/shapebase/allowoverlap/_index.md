---
title: ShapeBase.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: Aspose.Words för .NET
description: ShapeBase AllowOverlap fast egendom. Hämtar eller ställer in ett värde som anger om denna form kan överlappa andra former i C#.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing/shapebase/allowoverlap/
---
## ShapeBase.AllowOverlap property

Hämtar eller ställer in ett värde som anger om denna form kan överlappa andra former.

```csharp
public bool AllowOverlap { get; set; }
```

## Anmärkningar

Den här egenskapen påverkar beteendet hos formen i Microsoft Word. Aspose.Words ignorerar värdet på den här egenskapen.

Den här egenskapen är endast tillämplig på former på toppnivå.

Standardvärdet är`Sann`.

## Exempel

Visar hur man arbetar med egenskaper för flytande tabeller.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

if (table.TextWrapping == TextWrapping.Around)
{
    Assert.AreEqual(RelativeHorizontalPosition.Margin, table.HorizontalAnchor);
    Assert.AreEqual(RelativeVerticalPosition.Paragraph, table.VerticalAnchor);
    Assert.AreEqual(false, table.AllowOverlap);

    // Endast Marginal, Sida, Kolumn tillgängliga i RelativeHorizontalPosition för HorizontalAnchor Setter.
    // ArgumentException kommer att kastas för alla andra värden.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // Endast Marginal, Sida, Paragraph tillgängliga i RelativeVerticalPosition för VerticalAnchor Setter.
    // ArgumentException kommer att kastas för alla andra värden.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
