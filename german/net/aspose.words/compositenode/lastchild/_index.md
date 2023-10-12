---
title: CompositeNode.LastChild
second_title: Aspose.Words für .NET-API-Referenz
description: CompositeNode eigendom. Ruft das letzte untergeordnete Element des Knotens ab.
type: docs
weight: 50
url: /de/net/aspose.words/compositenode/lastchild/
---
## CompositeNode.LastChild property

Ruft das letzte untergeordnete Element des Knotens ab.

```csharp
public Node LastChild { get; }
```

### Bemerkungen

Wenn es keinen letzten untergeordneten Knoten gibt, a`Null` wird zurückgegeben.

### Beispiele

Zeigt, wie die Methoden von Node und CompositeNode verwendet werden, um einen Abschnitt vor dem letzten Abschnitt im Dokument zu entfernen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1 text.");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("Section 2 text.");

// Beide Abschnitte sind Geschwister voneinander.
Section lastSection = (Section)doc.LastChild;
Section firstSection = (Section)lastSection.PreviousSibling;

// Einen Abschnitt basierend auf seiner Geschwisterbeziehung mit einem anderen Abschnitt entfernen.
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

// Der Abschnitt, den wir entfernt haben, war der erste, so dass nur noch der zweite im Dokument übrig blieb.
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### Siehe auch

* class [Node](../../node/)
* class [CompositeNode](../)
* namensraum [Aspose.Words](../../compositenode/)
* Montage [Aspose.Words](../../../)


