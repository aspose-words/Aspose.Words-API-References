---
title: Granularity Enum
linktitle: Granularity
articleTitle: Granularity
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Comparing.Granularity-uppräkningen för att enkelt spåra dokumentändringar med precision. Förbättra din dokumentjämförelse idag!
type: docs
weight: 490
url: /sv/net/aspose.words.comparing/granularity/
---
## Granularity enumeration

Anger granulariteten för ändringar som ska spåras vid jämförelse av två dokument.

```csharp
public enum Granularity
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| CharLevel | `0` | Anger ändringar på teckennivå. |
| WordLevel | `1` | Anger ändringar på ordnivå. |

## Exempel

Visar för att ange en granularitet vid jämförelse av dokument.

```csharp
Document docA = new Document();
DocumentBuilder builderA = new DocumentBuilder(docA);
builderA.Writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

Document docB = new Document();
DocumentBuilder builderB = new DocumentBuilder(docB);
builderB.Writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Ange om ändringar spåras
// per tecken ('Granularity.CharLevel'), eller per ord ('Granularity.WordLevel').
CompareOptions compareOptions = new CompareOptions();
compareOptions.Granularity = granularity;

docA.Compare(docB, "author", DateTime.Now, compareOptions);

// Det första dokumentets samling av revisionsgrupper innehåller alla skillnader mellan dokumenten.
RevisionGroupCollection groups = docA.Revisions.Groups;
Assert.AreEqual(5, groups.Count);
```

### Se även

* namnutrymme [Aspose.Words.Comparing](../../aspose.words.comparing/)
* hopsättning [Aspose.Words](../../)
