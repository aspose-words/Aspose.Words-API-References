---
title: CompareOptions.Granularity
linktitle: Granularity
articleTitle: Granularity
second_title: Aspose.Words för .NET
description: Upptäck egenskapen CompareOptions Granularity, spåra ändringar per tecken eller ord för exakt textredigering. Förbättra din dokumentkontroll idag!
type: docs
weight: 40
url: /sv/net/aspose.words.comparing/compareoptions/granularity/
---
## CompareOptions.Granularity property

Anger om ändringar spåras per tecken eller per ord.

```csharp
public Granularity Granularity { get; set; }
```

## Anmärkningar

Standardvärdet ärWordLevel .

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

* enum [Granularity](../../granularity/)
* class [CompareOptions](../)
* namnutrymme [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* hopsättning [Aspose.Words](../../../)
