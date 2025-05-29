---
title: TabStopCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words für .NET
description: Greifen Sie mithilfe der TabStopCollection-Elementeigenschaft mühelos auf Tabstopps zu. Rufen Sie spezifische Stopps nach Index ab, um eine effiziente Benutzeroberflächennavigation zu ermöglichen.
type: docs
weight: 20
url: /de/net/aspose.words/tabstopcollection/item/
---
## TabStopCollection indexer (1 of 2)

Ruft einen Tabulatorstopp am angegebenen Index ab.

```csharp
public TabStop this[int index] { get; }
```

| Parameter | Beschreibung |
| --- | --- |
| index | Ein Index in der Sammlung von Tabstopps. |

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

---

## TabStopCollection indexer (2 of 2)

Ruft einen Tabulator an der angegebenen Position ab.

```csharp
public TabStop this[double position] { get; }
```

| Parameter | Beschreibung |
| --- | --- |
| position | Die Position (in Punkten) des Tabulatorstopps. |

## Bemerkungen

Rückgaben`null` wenn an der angegebenen Position kein Tabulatorstopp gefunden wird.

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
