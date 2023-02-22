---
title: CompositeNode.RemoveChild
second_title: Aspose.Words für .NET-API-Referenz
description: CompositeNode methode. Entfernt den angegebenen untergeordneten Knoten.
type: docs
weight: 180
url: /de/net/aspose.words/compositenode/removechild/
---
## CompositeNode.RemoveChild method

Entfernt den angegebenen untergeordneten Knoten.

```csharp
public Node RemoveChild(Node oldChild)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| oldChild | Node | Der zu entfernende Knoten. |

### Rückgabewert

Der entfernte Knoten.

### Bemerkungen

Das übergeordnete Element von oldChild wird auf null gesetzt, nachdem der Knoten entfernt wurde.

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

// Der Abschnitt, den wir entfernt haben, war der erste, sodass das Dokument nur den zweiten enthält.
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### Siehe auch

* class [Node](../../node/)
* class [CompositeNode](../)
* namensraum [Aspose.Words](../../compositenode/)
* Montage [Aspose.Words](../../../)


