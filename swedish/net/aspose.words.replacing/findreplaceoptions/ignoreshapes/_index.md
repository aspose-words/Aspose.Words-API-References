---
title: FindReplaceOptions.IgnoreShapes
linktitle: IgnoreShapes
articleTitle: IgnoreShapes
second_title: Aspose.Words för .NET
description: FindReplaceOptions IgnoreShapes fast egendom. Hämtar eller ställer in ett booleskt värde som indikerar att formerna i en text ska ignoreras i C#.
type: docs
weight: 110
url: /sv/net/aspose.words.replacing/findreplaceoptions/ignoreshapes/
---
## FindReplaceOptions.IgnoreShapes property

Hämtar eller ställer in ett booleskt värde som indikerar att formerna i en text ska ignoreras.

Standardvärdet är`falsk`.

```csharp
public bool IgnoreShapes { get; set; }
```

## Exempel

Visar hur du ignorerar former när du ersätter text.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertShape(ShapeType.Balloon, 200, 200);            
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder.Document.Range.Replace("Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit.", new FindReplaceOptions() { IgnoreShapes = true });
Assert.AreEqual("Lorem ipsum dolor sit amet, consectetur adipiscing elit.", builder.Document.GetText().Trim());
```

### Se även

* class [FindReplaceOptions](../)
* namnutrymme [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../../)
