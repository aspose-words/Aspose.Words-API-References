---
title: Granularity
second_title: Aspose.Words für .NET-API-Referenz
description: Gibt die Granularität der zu verfolgenden Änderungen an wenn zwei Dokumente verglichen werden.
type: docs
weight: 280
url: /de/net/aspose.words.comparing/granularity/
---
## Granularity enumeration

Gibt die Granularität der zu verfolgenden Änderungen an, wenn zwei Dokumente verglichen werden.

```csharp
public enum Granularity
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| CharLevel | `0` |  |
| WordLevel | `1` |  |

### Beispiele

Zeigt an, um beim Vergleichen von Dokumenten eine Granularität anzugeben.

```csharp
Document docA = new Document();
DocumentBuilder builderA = new DocumentBuilder(docA);
builderA.Writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

Document docB = new Document();
DocumentBuilder builderB = new DocumentBuilder(docB);
builderB.Writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Geben Sie an, ob Änderungen nachverfolgt werden
// nach Zeichen ('Granularity.CharLevel') oder nach Wort ('Granularity.WordLevel').
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.Granularity = granularity;

docA.Compare(docB, "author", DateTime.Now, compareOptions);

// Die Sammlung der Überarbeitungsgruppen des ersten Dokuments enthält alle Unterschiede zwischen Dokumenten.
RevisionGroupCollection groups = docA.Revisions.Groups;
Assert.AreEqual(5, groups.Count);
```

### Siehe auch

* namensraum [Aspose.Words.Comparing](../../aspose.words.comparing)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
