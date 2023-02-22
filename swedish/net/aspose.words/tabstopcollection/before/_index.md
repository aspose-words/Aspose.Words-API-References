---
title: TabStopCollection.Before
second_title: Aspose.Words för .NET API Referens
description: TabStopCollection metod. Får ett första tabbstopp till vänster om den angivna positionen.
type: docs
weight: 50
url: /sv/net/aspose.words/tabstopcollection/before/
---
## TabStopCollection.Before method

Får ett första tabbstopp till vänster om den angivna positionen.

```csharp
public TabStop Before(double position)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| position | Double | Referenspositionen (i punkter). |

### Returvärde

Ett tabbstoppobjekt eller noll om ett lämpligt tabbstopp inte hittades.

### Anmärkningar

Hoppar över tabbstopp med **Inriktning** satt till`TabAlignment.Bar`.

### Exempel

Visar hur man arbetar med ett dokuments samling av tabbstopp.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 poäng är en "tum" på tabbstoppslinjalen i Microsoft Word.
tabStops.Add(new TabStop(72.0));
tabStops.Add(new TabStop(432.0, TabAlignment.Right, TabLeader.Dashes));

Assert.AreEqual(2, tabStops.Count);
Assert.IsFalse(tabStops[0].IsClear);
Assert.IsFalse(tabStops[0].Equals(tabStops[1]));

// Varje "tab"-tecken tar byggarens markör till platsen för nästa tabbstopp.
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// Varje stycke får sin tabbstoppsamling, som klonar dess värden från dokumentbyggarens tabbstoppsamling.
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// En tabbstoppsamling kan peka oss till TabStops före och efter vissa positioner.
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

// Vi kan rensa ett styckes tabbstoppsamling för att återgå till standardbeteendet för tabbning.
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### Se även

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* namnutrymme [Aspose.Words](../../tabstopcollection/)
* hopsättning [Aspose.Words](../../../)


