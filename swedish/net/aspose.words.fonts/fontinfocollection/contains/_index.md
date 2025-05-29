---
title: FontInfoCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words för .NET
description: Upptäck om FontInfoCollection innehåller ett specifikt typsnitt. Hantera och få enkelt åtkomst till din typsnittssamling med denna viktiga metod.
type: docs
weight: 60
url: /sv/net/aspose.words.fonts/fontinfocollection/contains/
---
## FontInfoCollection.Contains method

Avgör om samlingen innehåller ett teckensnitt med det angivna namnet.

```csharp
public bool Contains(string name)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| name | String | Skiftlägeskänsligt namn på teckensnittet som ska hittas. |

### Returvärde

`sann`om föremålet finns i samlingen; annars,`falsk`.

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
