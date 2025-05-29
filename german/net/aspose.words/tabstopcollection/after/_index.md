---
title: TabStopCollection.After
linktitle: After
articleTitle: After
second_title: Aspose.Words für .NET
description: Entdecken Sie die Methode „TabStopCollection After“, um effizient den ersten Tabstopp rechts von Ihrer angegebenen Position abzurufen und so eine nahtlose Navigation zu ermöglichen.
type: docs
weight: 40
url: /de/net/aspose.words/tabstopcollection/after/
---
## TabStopCollection.After method

Ruft einen ersten Tabulatorstopp rechts von der angegebenen Position ab.

```csharp
public TabStop After(double position)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| position | Double | Die Referenzposition (in Punkten). |

### Rückgabewert

Ein Tabstoppobjekt oder`null` wenn kein passender Tabulator gefunden wurde.

## Bemerkungen

Überspringt Tabstopps mit[`Alignment`](../../tabstop/alignment/) eingestellt aufBar.

## Beispiele

Zeigt, wie mit der Tabstopp-Sammlung eines Dokuments gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 Punkte sind ein „Zoll“ auf dem Tabstopplineal von Microsoft Word.
tabStops.Add(new TabStop(72.0));
tabStops.Add(new TabStop(432.0, TabAlignment.Right, TabLeader.Dashes));

Assert.AreEqual(2, tabStops.Count);
Assert.IsFalse(tabStops[0].IsClear);
Assert.IsFalse(tabStops[0].Equals(tabStops[1]));

// Jedes „Tabulator“-Zeichen bringt den Cursor des Builders an die Position des nächsten Tabulatorstopps.
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// Jeder Absatz erhält seine Tabstopp-Sammlung, die ihre Werte aus der Tabstopp-Sammlung des Dokument-Generators klont.
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// Eine Tabstopp-Sammlung kann uns auf TabStops vor und nach bestimmten Positionen verweisen.
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

// Wir können die Tabstopp-Sammlung eines Absatzes löschen, um zum Standard-Tabulatorverhalten zurückzukehren.
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### Siehe auch

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
