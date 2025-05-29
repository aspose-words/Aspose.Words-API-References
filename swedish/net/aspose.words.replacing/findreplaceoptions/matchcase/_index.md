---
title: FindReplaceOptions.MatchCase
linktitle: MatchCase
articleTitle: MatchCase
second_title: Aspose.Words för .NET
description: Upptäck egenskapen MatchCase i FindReplaceOptions, aktivera jämförelser med eller utan skiftlägeskänslighet för exakt textredigering. Optimera ditt arbetsflöde!
type: docs
weight: 140
url: /sv/net/aspose.words.replacing/findreplaceoptions/matchcase/
---
## FindReplaceOptions.MatchCase property

Sant indikerar skiftlägeskänslig jämförelse, falskt indikerar skiftläges-okänslig jämförelse.

```csharp
public bool MatchCase { get; set; }
```

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

### Se även

* class [FindReplaceOptions](../)
* namnutrymme [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../../)
