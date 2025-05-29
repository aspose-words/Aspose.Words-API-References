---
title: CompositeNode.RemoveChild
linktitle: RemoveChild
articleTitle: RemoveChild
second_title: Aspose.Words für .NET
description: Verwalten Sie Ihren CompositeNode mühelos mit der RemoveChild-Methode, die das Entfernen von Knoten optimiert und so die Leistung und Effizienz verbessert.
type: docs
weight: 190
url: /de/net/aspose.words/compositenode/removechild/
---
## CompositeNode.RemoveChild&lt;T&gt; method

Entfernt den angegebenen untergeordneten Knoten.

```csharp
public T RemoveChild<T>(T oldChild)
    where T : Node
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| oldChild | T | Der zu entfernende Knoten. |

### Rückgabewert

Der entfernte Knoten.

## Bemerkungen

Das Elternteil von*oldChild* ist eingestellt auf`null` nachdem der Knoten entfernt wurde.

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
