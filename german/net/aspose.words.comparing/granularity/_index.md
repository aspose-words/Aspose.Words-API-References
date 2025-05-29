---
title: Granularity Enum
linktitle: Granularity
articleTitle: Granularity
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.Comparing.Granularity, um Dokumentänderungen mühelos und präzise zu verfolgen. Verbessern Sie noch heute Ihren Dokumentenvergleich!
type: docs
weight: 490
url: /de/net/aspose.words.comparing/granularity/
---
## Granularity enumeration

Gibt die Granularität der Änderungen an, die beim Vergleich zweier Dokumente verfolgt werden sollen.

```csharp
public enum Granularity
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| CharLevel | `0` | Gibt Änderungen auf Zeichenebene an. |
| WordLevel | `1` | Gibt Änderungen auf Wortebene an. |

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

* namensraum [Aspose.Words.Comparing](../../aspose.words.comparing/)
* Montage [Aspose.Words](../../)
