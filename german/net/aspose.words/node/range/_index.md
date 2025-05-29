---
title: Node.Range
linktitle: Range
articleTitle: Range
second_title: Aspose.Words für .NET
description: Entdecken Sie die Node Range-Eigenschaft und greifen Sie mühelos auf ein Range-Objekt zu, das das Dokumentsegment innerhalb Ihres Knotens definiert, um die Inhaltsverwaltung zu verbessern.
type: docs
weight: 80
url: /de/net/aspose.words/node/range/
---
## Node.Range property

Gibt einen[`Range`](../../range/)Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist.

```csharp
public Range Range { get; }
```

## Beispiele

Zeigt, wie alle Knoten aus einem Bereich gelöscht werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie dem ersten Abschnitt im Dokument Text hinzu und fügen Sie dann einen weiteren Abschnitt hinzu.
builder.Write("Section 1. ");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Write("Section 2.");

Assert.AreEqual("Section 1. \fSection 2.", doc.GetText().Trim());

// Entfernen Sie den ersten Abschnitt vollständig, indem Sie alle Knoten entfernen
// innerhalb seines Bereichs, einschließlich des Abschnitts selbst.
doc.Sections[0].Range.Delete();

Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual("Section 2.", doc.GetText().Trim());
```

### Siehe auch

* class [Range](../../range/)
* class [Node](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
