---
title: TabStopCollection Class
linktitle: TabStopCollection
articleTitle: TabStopCollection
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.TabStopCollection. Hantera enkelt anpassade tabbstopp för stycken och formateringar, och förbättra formateringen av ditt dokument med precision.
type: docs
weight: 7060
url: /sv/net/aspose.words/tabstopcollection/
---
## TabStopCollection class

En samling av[`TabStop`](../tabstop/) objekt som representerar anpassade flikar för ett stycke eller en stil.

För att lära dig mer, besök[Aspose.Words-dokumentobjektmodell (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) dokumentationsartikel.

```csharp
public class TabStopCollection : InternableComplexAttr
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words/tabstopcollection/count/) { get; } | Hämtar antalet tabbstopp i samlingen. |
| [Item](../../aspose.words/tabstopcollection/item/) { get; } | Hämtar ett tabbstopp vid det angivna indexet. (2 indexers) |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words/tabstopcollection/add/#add)(*[TabStop](../tabstop/)*) | Lägger till eller ersätter ett tabbstopp i samlingen. |
| [Add](../../aspose.words/tabstopcollection/add/#add_1)(*double, [TabAlignment](../tabalignment/), [TabLeader](../tableader/)*) | Lägger till eller ersätter ett tabbstopp i samlingen. |
| [After](../../aspose.words/tabstopcollection/after/)(*double*) | Hämtar ett första tabbstopp till höger om den angivna positionen. |
| [Before](../../aspose.words/tabstopcollection/before/)(*double*) | Hämtar ett första tabbstopp till vänster om den angivna positionen. |
| [Clear](../../aspose.words/tabstopcollection/clear/)() | Tar bort alla tabbstoppspositioner. |
| override [Equals](../../aspose.words/tabstopcollection/equals/#equals_1)(*object*) | Avgör om det angivna objektet har samma värde som det aktuella objektet. |
| [Equals](../../aspose.words/tabstopcollection/equals/#equals)(*TabStopCollection*) | Avgör om den angivna`TabStopCollection` är lika värdefullt som den nuvarande`TabStopCollection` . |
| override [GetHashCode](../../aspose.words/tabstopcollection/gethashcode/)() | Fungerar som en hashfunktion för den här typen. |
| [GetIndexByPosition](../../aspose.words/tabstopcollection/getindexbyposition/)(*double*) | Hämtar indexet för ett tabbstopp med den angivna positionen i punkter. |
| [GetPositionByIndex](../../aspose.words/tabstopcollection/getpositionbyindex/)(*int*) | Hämtar positionen (i punkter) för tabbstoppet vid det angivna indexet. |
| [RemoveByIndex](../../aspose.words/tabstopcollection/removebyindex/)(*int*) | Tar bort ett tabbstopp vid det angivna indexet från samlingen. |
| [RemoveByPosition](../../aspose.words/tabstopcollection/removebyposition/)(*double*) | Tar bort ett tabbstopp vid den angivna positionen från samlingen. |

## Anmärkningar

I Microsoft Word-dokument kan ett tabbstopp definieras i egenskaperna för en paragraph -stil eller direkt i egenskaperna för ett stycke. Ett format kan baseras på ett annat format. Därför är den kompletta uppsättningen tabbstopp för ett givet objekt en kombination av tabbstopp som definierats direkt på detta objekt och tabbstopp som ärvts från de överordnade formaten.

Med andra ord, när du får en`TabStopCollection` För ett stycke eller en stil innehåller den endast de anpassade tabbstopp som definierats direkt för detta stycke eller stil. Samlingen inkluderar inte tabbstopp som definierats i de överordnade stilarna eller standardtabbstopp.

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

* class [InternableComplexAttr](../internablecomplexattr/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
