---
title: FontInfoCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FontInfoCollection Count och hämta enkelt det totala antalet element i din samling för sömlös datahantering.
type: docs
weight: 10
url: /sv/net/aspose.words.fonts/fontinfocollection/count/
---
## FontInfoCollection.Count property

Hämtar antalet element som finns i samlingen.

```csharp
public int Count { get; }
```

## Exempel

Visar information om de teckensnitt som finns i det tomma dokumentet.

```csharp
Document doc = new Document();

// Ett tomt dokument innehåller 3 standardteckensnitt. Varje teckensnitt i dokumentet
// kommer att ha ett motsvarande FontInfo-objekt som innehåller information om det typsnittet.
Assert.AreEqual(3, doc.FontInfos.Count);

Assert.True(doc.FontInfos.Contains("Times New Roman"));
Assert.AreEqual(204, doc.FontInfos["Times New Roman"].Charset);

Assert.True(doc.FontInfos.Contains("Symbol"));
Assert.True(doc.FontInfos.Contains("Arial"));
```

### Se även

* class [FontInfoCollection](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
