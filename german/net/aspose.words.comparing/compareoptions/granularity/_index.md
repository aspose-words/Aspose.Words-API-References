---
title: CompareOptions.Granularity
linktitle: Granularity
articleTitle: Granularity
second_title: Aspose.Words für .NET
description: Entdecken Sie die CompareOptions-Granularitätseigenschaft und verfolgen Sie Änderungen zeichen- oder wortweise für präzise Textbearbeitung. Verbessern Sie noch heute Ihre Dokumentenkontrolle!
type: docs
weight: 40
url: /de/net/aspose.words.comparing/compareoptions/granularity/
---
## CompareOptions.Granularity property

Gibt an, ob Änderungen zeichenweise oder wortweise verfolgt werden.

```csharp
public Granularity Granularity { get; set; }
```

## Bemerkungen

Der Standardwert istWordLevel .

## Beispiele

Zeigt an, dass beim Vergleichen von Dokumenten eine Granularität angegeben werden muss.

```csharp
Document docA = new Document();
DocumentBuilder builderA = new DocumentBuilder(docA);
builderA.Writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

Document docB = new Document();
DocumentBuilder builderB = new DocumentBuilder(docB);
builderB.Writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Geben Sie an, ob Änderungen verfolgt werden
// nach Zeichen ('Granularity.CharLevel') oder nach Wort ('Granularity.WordLevel').
CompareOptions compareOptions = new CompareOptions();
compareOptions.Granularity = granularity;

docA.Compare(docB, "author", DateTime.Now, compareOptions);

// Die Sammlung von Revisionsgruppen des ersten Dokuments enthält alle Unterschiede zwischen den Dokumenten.
RevisionGroupCollection groups = docA.Revisions.Groups;
Assert.AreEqual(5, groups.Count);
```

### Siehe auch

* enum [Granularity](../../granularity/)
* class [CompareOptions](../)
* namensraum [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* Montage [Aspose.Words](../../../)
