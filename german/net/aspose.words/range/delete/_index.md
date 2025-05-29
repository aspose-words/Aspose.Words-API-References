---
title: Range.Delete
linktitle: Delete
articleTitle: Delete
second_title: Aspose.Words für .NET
description: Entfernen Sie effizient alle Zeichen innerhalb eines bestimmten Bereichs mit der Bereichslöschmethode. Vereinfachen Sie Ihre Textbearbeitung mühelos!
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

* class [Range](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
