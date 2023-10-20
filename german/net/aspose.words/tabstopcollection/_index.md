---
title: TabStopCollection Class
linktitle: TabStopCollection
articleTitle: TabStopCollection
second_title: Aspose.Words für .NET
description: Aspose.Words.TabStopCollection klas. Eine Sammlung vonTabStop Objekte die benutzerdefinierte Tabulatoren für einen Absatz oder einen Stil darstellen in C#.
type: docs
weight: 6210
url: /de/net/aspose.words/tabstopcollection/
---
## TabStopCollection class

Eine Sammlung von[`TabStop`](../tabstop/) Objekte, die benutzerdefinierte Tabulatoren für einen Absatz oder einen Stil darstellen.

Um mehr zu erfahren, besuchen Sie die[Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Dokumentationsartikel.

```csharp
public class TabStopCollection : InternableComplexAttr
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/tabstopcollection/count/) { get; } | Ruft die Anzahl der Tabstopps in der Sammlung ab. |
| [Item](../../aspose.words/tabstopcollection/item/) { get; } | Ruft einen Tabstopp am angegebenen Index ab. (2 indexers) |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words/tabstopcollection/add/#add)(*[TabStop](../tabstop/)*) | Fügt einen Tabstopp in der Sammlung hinzu oder ersetzt ihn. |
| [Add](../../aspose.words/tabstopcollection/add/#add_1)(*double, [TabAlignment](../tabalignment/), [TabLeader](../tableader/)*) | Fügt einen Tabstopp in der Sammlung hinzu oder ersetzt ihn. |
| [After](../../aspose.words/tabstopcollection/after/)(*double*) | Ruft einen ersten Tabstopp rechts von der angegebenen Position ab. |
| [Before](../../aspose.words/tabstopcollection/before/)(*double*) | Ruft einen ersten Tabstopp links von der angegebenen Position ab. |
| [Clear](../../aspose.words/tabstopcollection/clear/)() | Löscht alle Tabstopp-Positionen. |
| override [Equals](../../aspose.words/tabstopcollection/equals/#equals_1)(*object*) | Bestimmt, ob das angegebene Objekt den gleichen Wert wie das aktuelle Objekt hat. |
| [Equals](../../aspose.words/tabstopcollection/equals/#equals)(*TabStopCollection*) | Bestimmt, ob die angegebene`TabStopCollection` ist vom Wert her gleich dem Strom`TabStopCollection` . |
| override [GetHashCode](../../aspose.words/tabstopcollection/gethashcode/)() | Dient als Hash-Funktion für diesen Typ. |
| [GetIndexByPosition](../../aspose.words/tabstopcollection/getindexbyposition/)(*double*) | Ruft den Index eines Tabstopps mit der angegebenen Position in Punkten ab. |
| [GetPositionByIndex](../../aspose.words/tabstopcollection/getpositionbyindex/)(*int*) | Ruft die Position (in Punkt) des Tabstopps am angegebenen Index ab. |
| [RemoveByIndex](../../aspose.words/tabstopcollection/removebyindex/)(*int*) | Entfernt einen Tabstopp am angegebenen Index aus der Sammlung. |
| [RemoveByPosition](../../aspose.words/tabstopcollection/removebyposition/)(*double*) | Entfernt einen Tabstopp an der angegebenen Position aus der Sammlung. |

## Bemerkungen

In Microsoft Word-Dokumenten kann ein Tabstopp in den Eigenschaften eines Absatzstils oder direkt in den Eigenschaften eines Absatzes definiert werden. Ein Stil kann auf einem anderen Stil basieren. Daher ist der vollständige Satz von Tabstopps für ein bestimmtes Objekt eine Kombination aus direkt für dieses Objekt definierten Tabstopps und von den übergeordneten Stilen geerbten Tabstopps.

Wenn Sie in Aspose.Words eine erhalten`TabStopCollection`Für einen Absatz oder Stil enthält sie nur die benutzerdefinierten Tabstopps, die direkt für diesen Absatz oder Stil definiert wurden. Die Sammlung enthält keine Tabstopps, die in den übergeordneten Stilen oder Standardtabstopps definiert sind.

## Beispiele

Zeigt, wie mit der Sammlung von Tabstopps eines Dokuments gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 Punkte sind ein „Zoll“ auf dem Tabstopp-Lineal von Microsoft Word.
tabStops.Add(new TabStop(72.0));
tabStops.Add(new TabStop(432.0, TabAlignment.Right, TabLeader.Dashes));

Assert.AreEqual(2, tabStops.Count);
Assert.IsFalse(tabStops[0].IsClear);
Assert.IsFalse(tabStops[0].Equals(tabStops[1]));

// Jedes „Tab“-Zeichen bringt den Cursor des Builders an die Position des nächsten Tabstopps.
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// Jeder Absatz erhält seine Tabstopp-Sammlung, die seine Werte aus der Tabstopp-Sammlung des Document Builders klont.
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// Eine Tabstopp-Sammlung kann uns auf TabStops vor und nach bestimmten Positionen verweisen.
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

// Wir können die Tabstopp-Sammlung eines Absatzes löschen, um zum Standard-Tabbing-Verhalten zurückzukehren.
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### Siehe auch

* class [InternableComplexAttr](../internablecomplexattr/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
