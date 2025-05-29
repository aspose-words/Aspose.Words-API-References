---
title: TabStopCollection Class
linktitle: TabStopCollection
articleTitle: TabStopCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.TabStopCollection. Verwalten Sie ganz einfach benutzerdefinierte Tabstopps für Absätze und Stile und verbessern Sie die Formatierung Ihres Dokuments präzise.
type: docs
weight: 7060
url: /de/net/aspose.words/tabstopcollection/
---
## TabStopCollection class

Eine Sammlung von[`TabStop`](../tabstop/) Objekte, die benutzerdefinierte Registerkarten für einen Absatz oder einen Stil darstellen.

Um mehr zu erfahren, besuchen Sie die[Aspose.Words Dokumentobjektmodell (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Dokumentationsartikel.

```csharp
public class TabStopCollection : InternableComplexAttr
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/tabstopcollection/count/) { get; } | Ruft die Anzahl der Tabstopps in der Sammlung ab. |
| [Item](../../aspose.words/tabstopcollection/item/) { get; } | Ruft einen Tabulatorstopp am angegebenen Index ab. (2 indexers) |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words/tabstopcollection/add/#add)(*[TabStop](../tabstop/)*) | Fügt einen Tabulator in der Sammlung hinzu oder ersetzt ihn. |
| [Add](../../aspose.words/tabstopcollection/add/#add_1)(*double, [TabAlignment](../tabalignment/), [TabLeader](../tableader/)*) | Fügt einen Tabulator in der Sammlung hinzu oder ersetzt ihn. |
| [After](../../aspose.words/tabstopcollection/after/)(*double*) | Ruft einen ersten Tabulatorstopp rechts von der angegebenen Position ab. |
| [Before](../../aspose.words/tabstopcollection/before/)(*double*) | Ruft einen ersten Tabulatorstopp links von der angegebenen Position ab. |
| [Clear](../../aspose.words/tabstopcollection/clear/)() | Löscht alle Tabstopppositionen. |
| override [Equals](../../aspose.words/tabstopcollection/equals/#equals_1)(*object*) | Bestimmt, ob das angegebene Objekt den gleichen Wert wie das aktuelle Objekt hat. |
| [Equals](../../aspose.words/tabstopcollection/equals/#equals)(*TabStopCollection*) | Bestimmt, ob die angegebene`TabStopCollection` ist im Wert gleich dem aktuellen`TabStopCollection` . |
| override [GetHashCode](../../aspose.words/tabstopcollection/gethashcode/)() | Dient als Hash-Funktion für diesen Typ. |
| [GetIndexByPosition](../../aspose.words/tabstopcollection/getindexbyposition/)(*double*) | Ruft den Index eines Tabulators mit der angegebenen Position in Punkten ab. |
| [GetPositionByIndex](../../aspose.words/tabstopcollection/getpositionbyindex/)(*int*) | Ruft die Position (in Punkten) des Tabulatorstopps am angegebenen Index ab. |
| [RemoveByIndex](../../aspose.words/tabstopcollection/removebyindex/)(*int*) | Entfernt einen Tabulatorstopp am angegebenen Index aus der Auflistung. |
| [RemoveByPosition](../../aspose.words/tabstopcollection/removebyposition/)(*double*) | Entfernt einen Tabulator an der angegebenen Position aus der Auflistung. |

## Bemerkungen

In Microsoft Word-Dokumenten kann ein Tabstopp in den Eigenschaften eines Absatzstils oder direkt in den Eigenschaften eines Absatzes definiert werden. Ein Stil kann auf einem anderen Stil basieren. Daher ist der vollständige Tabstoppsatz für ein bestimmtes Objekt eine Kombination aus direkt für dieses Objekt definierten Tabstopps und von den übergeordneten Stilen übernommenen Tabstopps.

In Aspose.Words, wenn Sie eine`TabStopCollection` für einen Absatz oder einen Stil enthält es nur die benutzerdefinierten Tabstopps, die direkt für diesen Absatz oder Stil definiert sind. Die Sammlung enthält keine Tabstopps, die in den übergeordneten Stilen oder Standard-Tabstopps definiert sind.

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

* class [InternableComplexAttr](../internablecomplexattr/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
