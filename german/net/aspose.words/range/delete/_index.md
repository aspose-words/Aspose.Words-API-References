---
title: Range.Delete
linktitle: Delete
articleTitle: Delete
second_title: Aspose.Words für .NET
description: Range Delete methode. Löscht alle Zeichen des Bereichs in C#.
type: docs
weight: 70
url: /de/net/aspose.words/range/delete/
---
## Range.Delete method

Löscht alle Zeichen des Bereichs.

```csharp
public void Delete()
```

## Beispiele

Zeigt, wie alle Knoten aus einem Bereich gelöscht werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Text zum ersten Abschnitt im Dokument hinzufügen und dann einen weiteren Abschnitt hinzufügen.
builder.Write("Section 1. ");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Write("Section 2.");

Assert.AreEqual("Section 1. \fSection 2.", doc.GetText().Trim());

// Den ersten Abschnitt vollständig entfernen, indem alle Knoten entfernt werden
// innerhalb seines Bereichs, einschließlich des Abschnitts selbst.
doc.Sections[0].Range.Delete();

Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual("Section 2.", doc.GetText().Trim());
```

### Siehe auch

* class [Range](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
