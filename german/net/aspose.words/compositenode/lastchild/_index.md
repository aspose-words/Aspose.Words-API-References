---
title: CompositeNode.LastChild
linktitle: LastChild
articleTitle: LastChild
second_title: Aspose.Words für .NET
description: Entdecken Sie die CompositeNode LastChild-Eigenschaft, um einfach auf den letzten untergeordneten Knoten zuzugreifen und ihn zu bearbeiten und so Ihre Datenstrukturverwaltung zu verbessern.
type: docs
weight: 50
url: /de/net/aspose.words/compositenode/lastchild/
---
## CompositeNode.LastChild property

Ruft das letzte untergeordnete Element des Knotens ab.

```csharp
public Node LastChild { get; }
```

## Bemerkungen

Wenn es keinen letzten Kindknoten gibt,`null` wird zurückgegeben.

## Beispiele

Zeigt, wie man mit den Methoden von Node und CompositeNode einen Abschnitt vor dem letzten Abschnitt im Dokument entfernt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1 text.");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("Section 2 text.");

// Beide Abschnitte sind Geschwister voneinander.
Section lastSection = (Section)doc.LastChild;
Section firstSection = (Section)lastSection.PreviousSibling;

// Entfernen Sie einen Abschnitt basierend auf seiner Geschwisterbeziehung mit einem anderen Abschnitt.
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

// Wir haben den ersten Abschnitt entfernt, sodass im Dokument nur der zweite übrig blieb.
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### Siehe auch

* class [Node](../../node/)
* class [CompositeNode](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
