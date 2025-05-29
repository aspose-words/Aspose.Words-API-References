---
title: FindReplaceOptions Class
linktitle: FindReplaceOptions
articleTitle: FindReplaceOptions
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.FindReplaceOptions för avancerade sök- och ersättningsfunktioner, vilket förbättrar dokumentredigering med precision och flexibilitet.
type: docs
weight: 5350
url: /sv/net/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class

Anger alternativ för sök/ersätt-operationer.

För att lära dig mer, besök[Sök och ersätt](https://docs.aspose.com/words/net/find-and-replace/) dokumentationsartikel.

```csharp
public class FindReplaceOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FindReplaceOptions](findreplaceoptions/#constructor)() | Initierar en ny instans av FindReplaceOptions-klassen med standardinställningar. |
| [FindReplaceOptions](findreplaceoptions/#constructor_1)(*[FindReplaceDirection](../findreplacedirection/)*) | Initierar en ny instans av FindReplaceOptions-klassen med den angivna riktningen. |
| [FindReplaceOptions](findreplaceoptions/#constructor_3)(*[IReplacingCallback](../ireplacingcallback/)*) | Initierar en ny instans av FindReplaceOptions-klassen med den angivna ersättningsanropsfunktionen. |
| [FindReplaceOptions](findreplaceoptions/#constructor_2)(*[FindReplaceDirection](../findreplacedirection/), [IReplacingCallback](../ireplacingcallback/)*) | Initierar en ny instans av FindReplaceOptions-klassen med den angivna riktningen och ersättande callback. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [ApplyFont](../../aspose.words.replacing/findreplaceoptions/applyfont/) { get; } | Textformatering tillämpad på nytt innehåll. |
| [ApplyParagraphFormat](../../aspose.words.replacing/findreplaceoptions/applyparagraphformat/) { get; } | Styckeformatering tillämpad på nytt innehåll. |
| [Direction](../../aspose.words.replacing/findreplaceoptions/direction/) { get; set; } | Väljer riktning för ersättning. Standardvärdet ärForward . |
| [FindWholeWordsOnly](../../aspose.words.replacing/findreplaceoptions/findwholewordsonly/) { get; set; } | True indikerar att oldValue måste vara ett fristående ord. |
| [IgnoreDeleted](../../aspose.words.replacing/findreplaceoptions/ignoredeleted/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger att text i borttagna revisioner ska ignoreras. Standardvärdet är`falsk` . |
| [IgnoreFieldCodes](../../aspose.words.replacing/findreplaceoptions/ignorefieldcodes/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger att text i fältkoder ska ignoreras. Standardvärdet är`falsk` . |
| [IgnoreFields](../../aspose.words.replacing/findreplaceoptions/ignorefields/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger att text i fält ska ignoreras. Standardvärdet är`falsk` . |
| [IgnoreFootnotes](../../aspose.words.replacing/findreplaceoptions/ignorefootnotes/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger att fotnoter ska ignoreras. Standardvärdet är`falsk` . |
| [IgnoreInserted](../../aspose.words.replacing/findreplaceoptions/ignoreinserted/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger att antingen text i infogningsrevisioner ska ignoreras. Standardvärdet är`falsk` . |
| [IgnoreShapes](../../aspose.words.replacing/findreplaceoptions/ignoreshapes/) { get; set; } | Hämtar eller anger ett booleskt värde som anger att former i en text ska ignoreras. |
| [IgnoreStructuredDocumentTags](../../aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger att innehållet i antingen ska ignoreras[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) . Standardvärdet är`falsk` . |
| [LegacyMode](../../aspose.words.replacing/findreplaceoptions/legacymode/) { get; set; } | Hämtar eller ställer in ett booleskt värde som indikerar att den gamla sök/ersätt-algoritmen används. |
| [MatchCase](../../aspose.words.replacing/findreplaceoptions/matchcase/) { get; set; } | Sant indikerar skiftlägeskänslig jämförelse, falskt indikerar skiftläges-okänslig jämförelse. |
| [ReplacementFormat](../../aspose.words.replacing/findreplaceoptions/replacementformat/) { get; set; } | Anger formatet för ersättningen. Standard ärText . |
| [ReplacingCallback](../../aspose.words.replacing/findreplaceoptions/replacingcallback/) { get; set; } | Den användardefinierade metoden som anropas före varje ersättningsförekomst. |
| [SmartParagraphBreakReplacement](../../aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/) { get; set; } | Hämtar eller anger ett booleskt värde som anger att det är tillåtet att ersätta stycket break när det inte finns något nästa systerparagraf. |
| [UseLegacyOrder](../../aspose.words.replacing/findreplaceoptions/uselegacyorder/) { get; set; } | True indikerar att en textsökning utförs sekventiellt uppifrån och ned med hänsyn till textrutorna. Standardvärdet är`falsk` . |
| [UseSubstitutions](../../aspose.words.replacing/findreplaceoptions/usesubstitutions/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger om substitutioner inom ersättningsmönster ska kännas igen och användas. Standardvärdet är`falsk` . |

## Exempel

Visar hur man växlar mellan skiftlägeskänslighet och versalkänslighet när man utför en sök-och-ersätt-åtgärd.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Vi kan använda ett "FindReplaceOptions"-objekt för att modifiera sök-och-ersätt-processen.
FindReplaceOptions options = new FindReplaceOptions();

// Sätt flaggan "MatchCase" till "true" för att tillämpa skiftlägeskänslighet när strängar söks efter att ersättas.
// Sätt flaggan "MatchCase" till "false" för att ignorera skiftläge vid sökning efter text att ersätta.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

Visar hur man växlar mellan fristående sök-och-ersätt-åtgärder som endast avser ord.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Vi kan använda ett "FindReplaceOptions"-objekt för att modifiera sök-och-ersätt-processen.
FindReplaceOptions options = new FindReplaceOptions();

// Sätt flaggan "FindWholeWordsOnly" till "true" för att ersätta den funna texten om den inte är en del av ett annat ord.
// Sätt flaggan "FindWholeWordsOnly" till "false" för att ersätta all text oavsett dess omgivning.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### Se även

* namnutrymme [Aspose.Words.Replacing](../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../)
