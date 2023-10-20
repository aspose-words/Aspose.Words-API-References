---
title: Granularity Enum
linktitle: Granularity
articleTitle: Granularity
second_title: Aspose.Words für .NET
description: Aspose.Words.Comparing.Granularity opsomming. Gibt die Granularität der zu verfolgenden Änderungen beim Vergleich zweier Dokumente an in C#.
type: docs
weight: 290
url: /de/net/aspose.words.comparing/granularity/
---
## Granularity enumeration

Gibt die Granularität der zu verfolgenden Änderungen beim Vergleich zweier Dokumente an.

```csharp
public enum Granularity
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| CharLevel | `0` |  |
| WordLevel | `1` |  |

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

* namensraum [Aspose.Words.Comparing](../../aspose.words.comparing/)
* Montage [Aspose.Words](../../)
