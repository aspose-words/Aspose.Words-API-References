---
title: Node.PreviousSibling
linktitle: PreviousSibling
articleTitle: PreviousSibling
second_title: Aspose.Words für .NET
description: Entdecken Sie die Node PreviousSibling-Eigenschaft, um einfach auf den Knoten zuzugreifen, der vor Ihrem aktuellen Knoten liegt, und verbessern Sie so Ihre Fähigkeiten zur DOM-Manipulation.
type: docs
weight: 70
url: /de/net/aspose.words/node/previoussibling/
---
## Node.PreviousSibling property

Ruft den Knoten ab, der diesem Knoten unmittelbar vorausgeht.

```csharp
public Node PreviousSibling { get; }
```

## Bemerkungen

Wenn es keinen vorhergehenden Knoten gibt,`null` wird zurückgegeben.

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

* class [Node](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
