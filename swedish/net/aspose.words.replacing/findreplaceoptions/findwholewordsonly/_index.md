---
title: FindReplaceOptions.FindWholeWordsOnly
second_title: Aspose.Words för .NET API Referens
description: FindReplaceOptions fast egendom. True anger att oldValue måste vara ett fristående ord.
type: docs
weight: 50
url: /sv/net/aspose.words.replacing/findreplaceoptions/findwholewordsonly/
---
## FindReplaceOptions.FindWholeWordsOnly property

True anger att oldValue måste vara ett fristående ord.

```csharp
public bool FindWholeWordsOnly { get; set; }
```

### Exempel

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

* class [FindReplaceOptions](../)
* namnutrymme [Aspose.Words.Replacing](../../findreplaceoptions/)
* hopsättning [Aspose.Words](../../../)


