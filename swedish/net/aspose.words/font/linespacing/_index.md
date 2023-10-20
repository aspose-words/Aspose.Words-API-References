---
title: Font.LineSpacing
linktitle: LineSpacing
articleTitle: LineSpacing
second_title: Aspose.Words för .NET
description: Font LineSpacing fast egendom. Returnerar radavstånd för detta teckensnitt i punkter i C#.
type: docs
weight: 190
url: /sv/net/aspose.words/font/linespacing/
---
## Font.LineSpacing property

Returnerar radavstånd för detta teckensnitt (i punkter).

```csharp
public double LineSpacing { get; }
```

## Exempel

Visar hur man får ett teckensnitts radavstånd, i punkter.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ställ in olika typsnitt för DocumentBuilder och verifiera deras radavstånd.
builder.Font.Name = "Calibri";
Assert.AreEqual(14.6484375d, builder.Font.LineSpacing);

builder.Font.Name = "Times New Roman";
Assert.AreEqual(13.798828125d, builder.Font.LineSpacing);
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
