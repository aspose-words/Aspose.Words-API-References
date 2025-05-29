---
title: ShapeBase.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: Aspose.Words för .NET
description: Upptäck ShapeBase AllowOverlap-egenskapen och styr forminteraktioner genom att aktivera eller inaktivera överlappning med andra former för ökad designflexibilitet.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing/shapebase/allowoverlap/
---
## ShapeBase.AllowOverlap property

Hämtar eller anger ett värde som anger om denna form kan överlappa andra former.

```csharp
public bool AllowOverlap { get; set; }
```

## Anmärkningar

Den här egenskapen påverkar formens beteende i Microsoft Word. Aspose.Words ignorerar värdet för den här egenskapen.

Den här egenskapen gäller endast för former på översta nivån.

Standardvärdet är`sann`.

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

    // Endast marginal, sida och kolumn är tillgängliga i RelativeHorizontalPosition för HorizontalAnchor-sättaren.
    // ArgumentException kommer att utlösas för alla andra värden.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // Endast marginal, sida och stycke tillgängliga i RelativeVerticalPosition för VerticalAnchor-inställaren.
    // ArgumentException kommer att utlösas för alla andra värden.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
