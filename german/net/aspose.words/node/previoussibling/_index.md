---
title: Node.PreviousSibling
linktitle: PreviousSibling
articleTitle: PreviousSibling
second_title: Aspose.Words für .NET
description: Node PreviousSibling eigendom. Ruft den Knoten ab der diesem Knoten unmittelbar vorangeht in C#.
type: docs
weight: 70
url: /de/net/aspose.words/node/previoussibling/
---
## Node.PreviousSibling property

Ruft den Knoten ab, der diesem Knoten unmittelbar vorangeht.

```csharp
public Node PreviousSibling { get; }
```

## Bemerkungen

Wenn kein vorhergehender Knoten vorhanden ist, a`Null` wird zurückgegeben.

## Beispiele

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

* class [Node](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
