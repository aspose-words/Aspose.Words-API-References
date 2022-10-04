---
title: TabStopCollection
second_title: Aspose.Words für .NET-API-Referenz
description: Eine Sammlung vonTabStop./tabstop/Objekte die benutzerdefinierte Tabulatoren für einen Absatz oder eine Formatvorlage darstellen.
type: docs
weight: 5910
url: /de/net/aspose.words/tabstopcollection/
---
## TabStopCollection class

Eine Sammlung von[`TabStop`](../tabstop/)Objekte, die benutzerdefinierte Tabulatoren für einen Absatz oder eine Formatvorlage darstellen.

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
| [Add](../../aspose.words/tabstopcollection/add/#add)(TabStop) | Fügt einen Tabstopp in der Sammlung hinzu oder ersetzt ihn. |
| [Add](../../aspose.words/tabstopcollection/add/#add_1)(double, TabAlignment, TabLeader) | Fügt einen Tabstopp in der Sammlung hinzu oder ersetzt ihn. |
| [After](../../aspose.words/tabstopcollection/after/)(double) | Ruft einen ersten Tabstopp rechts von der angegebenen Position ab. |
| [Before](../../aspose.words/tabstopcollection/before/)(double) | Ruft einen ersten Tabstopp links von der angegebenen Position ab. |
| [Clear](../../aspose.words/tabstopcollection/clear/)() | Löscht alle Tabulatorpositionen. |
| override [Equals](../../aspose.words/tabstopcollection/equals/#equals_1)(object) | Bestimmt, ob das angegebene Objekt im Wert dem aktuellen Objekt entspricht. |
| [Equals](../../aspose.words/tabstopcollection/equals/#equals)(TabStopCollection) | Bestimmt, ob die angegebene TabStopCollection im Wert der aktuellen TabStopCollection entspricht. |
| override [GetHashCode](../../aspose.words/tabstopcollection/gethashcode/)() | Dient als Hash-Funktion für diesen Typ. |
| [GetIndexByPosition](../../aspose.words/tabstopcollection/getindexbyposition/)(double) | Ruft den Index eines Tabstopps mit der angegebenen Position in Punkten ab. |
| [GetPositionByIndex](../../aspose.words/tabstopcollection/getpositionbyindex/)(int) | Ruft die Position (in Punkten) des Tabstopps am angegebenen Index ab. |
| [RemoveByIndex](../../aspose.words/tabstopcollection/removebyindex/)(int) | Entfernt einen Tabstopp am angegebenen Index aus der Sammlung. |
| [RemoveByPosition](../../aspose.words/tabstopcollection/removebyposition/)(double) | Entfernt einen Tabstopp an der angegebenen Position aus der Sammlung. |

### Bemerkungen

In Microsoft Word-Dokumenten kann ein Tabstopp in den Eigenschaften einer Absatz -Formatvorlage oder direkt in den Eigenschaften eines Absatzes definiert werden. Ein Stil kann auf einem anderen Stil basieren. Daher ist der vollständige Satz von Tabstopps für ein bestimmtes Objekt eine Kombination aus Tabstopps , die direkt für dieses Objekt definiert sind, und Tabstopps, die von den übergeordneten Stilen geerbt wurden.

Wenn Sie in Aspose.Words a **Tabstopps** Sammlung für einen Absatz oder eine Formatvorlage, enthält sie nur die benutzerdefinierten Tabulatoren, die direkt für diesen Absatz oder diese Formatvorlage definiert sind. Die Sammlung enthält keine Tabstopps, die in den übergeordneten Formatvorlagen oder Standardtabstopps definiert sind.

### Beispiele

Zeigt, wie Sie mit der Sammlung von Tabstopps eines Dokuments arbeiten.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 Punkte sind ein "Zoll" auf dem Microsoft Word-Tabulatorlineal.
tabStops.Add(new TabStop(72.0));
tabStops.Add(new TabStop(432.0, TabAlignment.Right, TabLeader.Dashes));

Assert.AreEqual(2, tabStops.Count);
Assert.IsFalse(tabStops[0].IsClear);
Assert.IsFalse(tabStops[0].Equals(tabStops[1]));

// Jedes "Tab"-Zeichen bringt den Cursor des Builders an die Position des nächsten Tabstopps.
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// Jeder Absatz erhält seine Tabstopp-Sammlung, die seine Werte aus der Tabstopp-Sammlung des Dokumentenerstellers klont.
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// Eine Tabstop-Sammlung kann uns auf TabStops vor und nach bestimmten Positionen verweisen.
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

// Wir können die Tabstopp-Sammlung eines Absatzes löschen, um zum Standard-Tab-Verhalten zurückzukehren.
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### Siehe auch

* class [InternableComplexAttr](../internablecomplexattr/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
