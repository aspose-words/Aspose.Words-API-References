---
title: TabStop.TabStop
second_title: Aspose.Words für .NET-API-Referenz
description: TabStop constructeur. Initialisiert eine neue Instanz dieser Klasse.
type: docs
weight: 10
url: /de/net/aspose.words/tabstop/tabstop/
---
## TabStop(double) {#constructor}

Initialisiert eine neue Instanz dieser Klasse.

```csharp
public TabStop(double position)
```

### Beispiele

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

* class [TabStop](../)
* namensraum [Aspose.Words](../../tabstop/)
* Montage [Aspose.Words](../../../)

---

## TabStop(double, TabAlignment, TabLeader) {#constructor_1}

Initialisiert eine neue Instanz dieser Klasse.

```csharp
public TabStop(double position, TabAlignment alignment, TabLeader leader)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| position | Double | Die Position des Tabstopps in Punkten. |
| alignment | TabAlignment | A[`TabAlignment`](../../tabalignment/) Der Wert that gibt die Ausrichtung des Texts an diesem Tabstopp an. |
| leader | TabLeader | A[`TabLeader`](../../tableader/) Wert, der den Typ der Führungslinie angibt, die unter dem Tabulatorzeichen angezeigt wird. |

### Beispiele

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

* enum [TabAlignment](../../tabalignment/)
* enum [TabLeader](../../tableader/)
* class [TabStop](../)
* namensraum [Aspose.Words](../../tabstop/)
* Montage [Aspose.Words](../../../)


