---
title: TabStopCollection.After
linktitle: After
articleTitle: After
second_title: Aspose.Words för .NET
description: Upptäck TabStopCollection After-metoden för att effektivt hämta den första tabbstoppen till höger om din angivna position för sömlös navigering.
type: docs
weight: 40
url: /sv/net/aspose.words/tabstopcollection/after/
---
## TabStopCollection.After method

Hämtar ett första tabbstopp till höger om den angivna positionen.

```csharp
public TabStop After(double position)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| position | Double | Referenspositionen (i punkter). |

### Returvärde

Ett tabbstoppobjekt eller`null` om en lämplig tabulatur inte hittades.

## Anmärkningar

Hoppar över tabbstopp med[`Alignment`](../../tabstop/alignment/) inställd påBar.

## Exempel

Visar hur man arbetar med ett dokuments samling av tabbstopp.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 punkter är en "tum" på tabbstoppslinjalen i Microsoft Word.
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

// En tabulatursamling kan peka oss till tabulaturer före och efter vissa positioner.
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
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
