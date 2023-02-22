---
title: CompareOptions.Granularity
second_title: Aspose.Words för .NET API Referens
description: CompareOptions fast egendom. Anger om ändringar spåras med tecken eller ord. Standardvärdet ärWordLevel .
type: docs
weight: 20
url: /sv/net/aspose.words.comparing/compareoptions/granularity/
---
## CompareOptions.Granularity property

Anger om ändringar spåras med tecken eller ord. Standardvärdet ärWordLevel .

```csharp
public Granularity Granularity { get; set; }
```

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

* enum [Granularity](../../granularity/)
* class [CompareOptions](../)
* namnutrymme [Aspose.Words.Comparing](../../compareoptions/)
* hopsättning [Aspose.Words](../../../)


