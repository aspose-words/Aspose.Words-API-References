---
title: FindReplaceOptions.IgnoreShapes
linktitle: IgnoreShapes
articleTitle: IgnoreShapes
second_title: Aspose.Words för .NET
description: Upptäck egenskapen IgnoreShapes i FindReplaceOptions. Kontrollera inkludering av former i textbehandling med denna viktiga booleska inställning för förbättrad noggrannhet.
type: docs
weight: 110
url: /sv/net/aspose.words.replacing/findreplaceoptions/ignoreshapes/
---
## FindReplaceOptions.IgnoreShapes property

Hämtar eller anger ett booleskt värde som anger att former i en text ska ignoreras.

Standardvärdet är`falsk`.

```csharp
public bool IgnoreShapes { get; set; }
```

## Exempel

Visar hur man ignorerar former när man ersätter text.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertShape(ShapeType.Balloon, 200, 200);
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

FindReplaceOptions findReplaceOptions = new FindReplaceOptions() { IgnoreShapes = true };
builder.Document.Range.Replace("Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit.", findReplaceOptions);
Assert.AreEqual("Lorem ipsum dolor sit amet, consectetur adipiscing elit.", builder.Document.GetText().Trim());
```

### Se även

* class [FindReplaceOptions](../)
* namnutrymme [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../../)
