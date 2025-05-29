---
title: FindReplaceOptions.FindWholeWordsOnly
linktitle: FindWholeWordsOnly
articleTitle: FindWholeWordsOnly
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen FindWholeWordsOnly förbättrar din sökning med korrekta resultat, vilket säkerställer att oldValue bara matchar som ett fristående ord.
type: docs
weight: 50
url: /sv/net/aspose.words.replacing/findreplaceoptions/findwholewordsonly/
---
## FindReplaceOptions.FindWholeWordsOnly property

True indikerar att oldValue måste vara ett fristående ord.

```csharp
public bool FindWholeWordsOnly { get; set; }
```

## Exempel

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

* class [FindReplaceOptions](../)
* namnutrymme [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../../)
