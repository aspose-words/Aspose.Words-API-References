---
title: Splitter Class
linktitle: Splitter
articleTitle: Splitter
second_title: Aspose.Words för .NET
description: Dela dokument enkelt med klassen Aspose.Words.LowCode.Splitter. Använd mångsidiga metoder för exakt dokumenthantering och förbättrad arbetsflödeseffektivitet.
type: docs
weight: 4420
url: /sv/net/aspose.words.lowcode/splitter/
---
## Splitter class

Tillhandahåller metoder avsedda att dela upp dokumenten i delar med hjälp av olika kriterier.

```csharp
public class Splitter : Processor
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| static [Create](../../aspose.words.lowcode/splitter/create/)(*[SplitterContext](../splittercontext/)*) | Skapar en ny instans av splitterprocessorn. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Utför processoråtgärden. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Anger indatadokument för bearbetning. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Anger indatadokument för bearbetning. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Anger listan över utdatadokumentströmmar. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Anger listan över utdatadokumentströmmar. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Anger utdataströmmen för processorn. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Anger utdataströmmen för processorn. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Anger utdatafilen för processorn. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Anger utdatafilen för processorn. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_4)(*string, string, int, int*) | Extraherar ett angivet sidintervall från en dokumentfil och sparar de extraherade sidorna till en ny fil. Utdatafilformatet bestäms av filändelsen på utdatafilnamnet. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), int, int*) | Extraherar ett angivet sidintervall från en dokumentström och sparar de extraherade sidorna till en utdataström med det angivna sparformatet. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_1)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), int, int*) | Extraherar ett angivet sidintervall från en dokumentström och sparar de extraherade sidorna till en utdataström med det angivna sparformatet. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_2)(*string, string, [SaveFormat](../../aspose.words/saveformat/), int, int*) | Extraherar ett angivet sidintervall från en dokumentfil och sparar de extraherade sidorna till en ny fil med det angivna sparformatet. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_3)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), int, int*) | Extraherar ett angivet sidintervall från en dokumentfil och sparar de extraherade sidorna till en ny fil med det angivna sparformatet. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_2)(*string, string*) | Tar bort tomma sidor från dokumentet och sparar resultatet. Returnerar en lista över sidnummer som togs bort. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Tar bort tomma sidor från ett dokument som tillhandahålls i en indataström och sparar det uppdaterade dokumentet till en utdataström i det angivna sparformatet. Returnerar en lista över sidnummer som togs bort. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_1)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Tar bort tomma sidor från ett dokument som tillhandahålls i en indataström och sparar det uppdaterade dokumentet till en utdataström i det angivna sparformatet. Returnerar en lista över sidnummer som togs bort. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_3)(*string, string, [SaveFormat](../../aspose.words/saveformat/)*) | Tar bort tomma sidor från dokumentet och sparar resultatet i det angivna formatet. Returnerar en lista över sidnummer som togs bort. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_4)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Tar bort tomma sidor från dokumentet och sparar resultatet i det angivna formatet. Returnerar en lista över sidnummer som togs bort. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split)(*Stream, [SaveFormat](../../aspose.words/saveformat/), [SplitOptions](../splitoptions/)*) | Delar upp ett dokument från en indataström i flera delar baserat på de angivna delningsalternativen och returnerar de resulterande delarna som en array av strömmar i det angivna sparformatet. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_1)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), [SplitOptions](../splitoptions/)*) | Delar upp ett dokument från en indataström i flera delar baserat på de angivna delningsalternativen och returnerar de resulterande delarna som en array av strömmar i det angivna sparformatet. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_2)(*string, string, [SplitOptions](../splitoptions/)*) | Delar upp ett dokument i flera delar baserat på de angivna delningsalternativen och sparar de resulterande delarna till filer. Utdatafilformatet bestäms av filändelsen på utdatafilnamnet. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_3)(*string, string, [SaveFormat](../../aspose.words/saveformat/), [SplitOptions](../splitoptions/)*) | Delar upp ett dokument i flera delar baserat på de angivna delningsalternativen och sparar de resulterande delarna till filer i det angivna sparformatet. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_4)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), [SplitOptions](../splitoptions/)*) | Delar upp ett dokument i flera delar baserat på de angivna delningsalternativen och sparar de resulterande delarna till filer i det angivna sparformatet. |

### Se även

* class [Processor](../processor/)
* namnutrymme [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../)
