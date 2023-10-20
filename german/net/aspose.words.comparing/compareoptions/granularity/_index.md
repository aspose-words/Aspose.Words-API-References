---
title: CompareOptions.Granularity
linktitle: Granularity
articleTitle: Granularity
second_title: Aspose.Words für .NET
description: CompareOptions Granularity eigendom. Gibt an ob Änderungen nach Zeichen oder Wort verfolgt werden. Der Standardwert istWordLevel  in C#.
type: docs
weight: 30
url: /de/net/aspose.words.comparing/compareoptions/granularity/
---
## CompareOptions.Granularity property

Gibt an, ob Änderungen nach Zeichen oder Wort verfolgt werden. Der Standardwert istWordLevel .

```csharp
public Granularity Granularity { get; set; }
```

## Beispiele

Wird angezeigt, um beim Vergleichen von Dokumenten eine Granularität anzugeben.

```csharp
Document docA = new Document();
DocumentBuilder builderA = new DocumentBuilder(docA);
builderA.Writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

Document docB = new Document();
DocumentBuilder builderB = new DocumentBuilder(docB);
builderB.Writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Geben Sie an, ob Änderungen nachverfolgt werden sollen
// nach Zeichen ('Granularity.CharLevel') oder nach Wort ('Granularity.WordLevel').
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.Granularity = granularity;

docA.Compare(docB, "author", DateTime.Now, compareOptions);

// Die Revisionsgruppensammlung des ersten Dokuments enthält alle Unterschiede zwischen Dokumenten.
RevisionGroupCollection groups = docA.Revisions.Groups;
Assert.AreEqual(5, groups.Count);
```

### Siehe auch

* enum [Granularity](../../granularity/)
* class [CompareOptions](../)
* namensraum [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* Montage [Aspose.Words](../../../)
