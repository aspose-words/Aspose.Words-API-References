---
title: NodeCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words für .NET
description: Entfernen Sie mühelos Knoten aus Ihrer Sammlung mit der NodeCollection RemoveAt-Methode. Optimieren Sie die Dokumentenverwaltung, indem Sie bestimmte Knoten schnell entfernen.
type: docs
weight: 100
url: /de/net/aspose.words/nodecollection/removeat/
---
## NodeCollection.RemoveAt method

Entfernt den Knoten am angegebenen Index aus der Sammlung und aus dem Dokument.

```csharp
public void RemoveAt(int index)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | Int32 | Der nullbasierte Index des Knotens. Negative Indizes sind zulässig und zeigen den Zugriff vom Ende der Liste an. Beispielsweise bedeutet -1 den letzten Knoten, -2 den vorletzten und so weiter. |

## Beispiele

Zeigt, wie Abschnitte in einem Dokument hinzugefügt und entfernt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// Löschen Sie den ersten Abschnitt aus dem Dokument.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// Fügen Sie eine Kopie des jetzigen ersten Abschnitts an das Ende des Dokuments an.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

### Siehe auch

* class [NodeCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
