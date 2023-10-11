---
title: Enum Granularity
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Comparing.Granularity uppräkning. Anger granulariteten för ändringar som ska spåras när två dokument jämförs.
type: docs
weight: 290
url: /sv/net/aspose.words.comparing/granularity/
---
## Granularity enumeration

Anger granulariteten för ändringar som ska spåras när två dokument jämförs.

```csharp
public enum Granularity
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| CharLevel | `0` |  |
| WordLevel | `1` |  |

### Exempel

Visar för att specificera en granularitet vid jämförelse av dokument.

```csharp
Document docA = new Document();
DocumentBuilder builderA = new DocumentBuilder(docA);
builderA.Writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

Document docB = new Document();
DocumentBuilder builderB = new DocumentBuilder(docB);
builderB.Writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Ange om ändringarna spåras
// efter tecken ('Granularity.CharLevel'), eller efter ord ('Granularity.WordLevel').
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.Granularity = granularity;

docA.Compare(docB, "author", DateTime.Now, compareOptions);

// Det första dokumentets samling av revisionsgrupper innehåller alla skillnader mellan dokument.
RevisionGroupCollection groups = docA.Revisions.Groups;
Assert.AreEqual(5, groups.Count);
```

### Se även

* namnutrymme [Aspose.Words.Comparing](../../aspose.words.comparing/)
* hopsättning [Aspose.Words](../../)


