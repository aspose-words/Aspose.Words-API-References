---
title: Class FindReplaceOptions
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Replacing.FindReplaceOptions klass. Anger alternativ för sök/ersättoperationer.
type: docs
weight: 4360
url: /sv/net/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class

Anger alternativ för sök-/ersätt-operationer.

```csharp
public class FindReplaceOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FindReplaceOptions](findreplaceoptions/#constructor)() | Default_Constructor |
| [FindReplaceOptions](findreplaceoptions/#constructor_1)(FindReplaceDirection) |  |
| [FindReplaceOptions](findreplaceoptions/#constructor_3)(IReplacingCallback) |  |
| [FindReplaceOptions](findreplaceoptions/#constructor_2)(FindReplaceDirection, IReplacingCallback) |  |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [ApplyFont](../../aspose.words.replacing/findreplaceoptions/applyfont/) { get; } | Textformatering tillämpas på nytt innehåll. |
| [ApplyParagraphFormat](../../aspose.words.replacing/findreplaceoptions/applyparagraphformat/) { get; } | Styckeformatering tillämpas på nytt innehåll. |
| [Direction](../../aspose.words.replacing/findreplaceoptions/direction/) { get; set; } | Väljer riktning för ersättning. Standardvärdet ärForward . |
| [FindWholeWordsOnly](../../aspose.words.replacing/findreplaceoptions/findwholewordsonly/) { get; set; } | True anger att oldValue måste vara ett fristående ord. |
| [IgnoreDeleted](../../aspose.words.replacing/findreplaceoptions/ignoredeleted/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger att texten i raderingsversioner ska ignoreras. Standardvärdet är`falsk` . |
| [IgnoreFieldCodes](../../aspose.words.replacing/findreplaceoptions/ignorefieldcodes/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger att text i fältkoder ska ignoreras. Standardvärdet är`falsk` . |
| [IgnoreFields](../../aspose.words.replacing/findreplaceoptions/ignorefields/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger att texten i fält ska ignoreras. Standardvärdet är`falsk` . |
| [IgnoreFootnotes](../../aspose.words.replacing/findreplaceoptions/ignorefootnotes/) { get; set; } | Hämtar eller ställer in ett booleskt värde som indikerar att antingen ignorera fotnoter. Standardvärdet är`falsk` . |
| [IgnoreInserted](../../aspose.words.replacing/findreplaceoptions/ignoreinserted/) { get; set; } | Hämtar eller ställer in ett booleskt värde som indikerar att texten i infogningsversioner ska ignoreras. Standardvärdet är`falsk` . |
| [LegacyMode](../../aspose.words.replacing/findreplaceoptions/legacymode/) { get; set; } | Hämtar eller ställer in ett booleskt värde som indikerar att gammal hitta/ersätt algoritm används. |
| [MatchCase](../../aspose.words.replacing/findreplaceoptions/matchcase/) { get; set; } | True indikerar skiftlägeskänslig jämförelse, false indikerar skiftlägesokänslig jämförelse. |
| [ReplacingCallback](../../aspose.words.replacing/findreplaceoptions/replacingcallback/) { get; set; } | Den användardefinierade metoden som anropas före varje ersättningsförekomst. |
| [SmartParagraphBreakReplacement](../../aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger att det är tillåtet att ersätta stycke break när det inte finns något nästa syskonstycke. |
| [UseLegacyOrder](../../aspose.words.replacing/findreplaceoptions/uselegacyorder/) { get; set; } | True indikerar att en textsökning utförs sekventiellt uppifrån och ned med tanke på textrutorna. Standardvärdet är false. |
| [UseSubstitutions](../../aspose.words.replacing/findreplaceoptions/usesubstitutions/) { get; set; } | Hämtar eller ställer in ett booleskt värde som indikerar om ersättningar ska identifieras och användas inom ersättningsmönster. Standardvärdet är`falsk` . |

### Exempel

Visar hur du växlar skiftlägeskänslighet när du utför en sök-och-ersätt-åtgärd.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Vi kan använda ett "FindReplaceOptions"-objekt för att ändra sök-och-ersätt-processen.
FindReplaceOptions options = new FindReplaceOptions();

// Ställ in "MatchCase"-flaggan till "true" för att tillämpa skiftlägeskänslighet samtidigt som du hittar strängar att ersätta.
// Ställ in "MatchCase"-flaggan till "false" för att ignorera skiftläge när du söker efter text som ska ersättas.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

Visar hur du växlar fristående sök-och-ersätt-operationer för endast ord.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Vi kan använda ett "FindReplaceOptions"-objekt för att ändra sök-och-ersätt-processen.
FindReplaceOptions options = new FindReplaceOptions();

// Ställ in "FindWholeWordsOnly"-flaggan till "true" för att ersätta den hittade texten om den inte är en del av ett annat ord.
// Ställ in "FindWholeWordsOnly"-flaggan till "false" för att ersätta all text oavsett omgivning.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### Se även

* namnutrymme [Aspose.Words.Replacing](../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../)


