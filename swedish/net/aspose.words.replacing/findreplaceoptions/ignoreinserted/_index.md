---
title: FindReplaceOptions.IgnoreInserted
linktitle: IgnoreInserted
articleTitle: IgnoreInserted
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FindReplaceOptions IgnoreInserted och styr texthanteringen i infogningsrevisioner med denna enkla booleska inställning. Standardinställningen är falsk.
type: docs
weight: 100
url: /sv/net/aspose.words.replacing/findreplaceoptions/ignoreinserted/
---
## FindReplaceOptions.IgnoreInserted property

Hämtar eller ställer in ett booleskt värde som anger att antingen text i infogningsrevisioner ska ignoreras. Standardvärdet är`falsk` .

```csharp
public bool IgnoreInserted { get; set; }
```

## Exempel

Visar hur man inkluderar eller ignorerar text i infogningsrevideringar under en sök-och-ersätt-åtgärd.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Börja spåra revisioner och infoga ett stycke. Det stycket kommer att vara en infogningsrevision.
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("Hello again!");
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsInsertRevision);

// Vi kan använda ett "FindReplaceOptions"-objekt för att modifiera sök-och-ersätt-processen.
FindReplaceOptions options = new FindReplaceOptions();

// Sätt flaggan "IgnoreInserted" till "true" för att få sök-och-ersätt-funktionen
// operation för att ignorera stycken som är infogningsrevideringar.
// Sätt flaggan "IgnoreInserted" till "false" för att få sök-och-ersätt-funktionen
// operation för att även söka efter text inuti infogningsrevisioner.
options.IgnoreInserted = ignoreTextInsideInsertRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideInsertRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### Se även

* class [FindReplaceOptions](../)
* namnutrymme [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../../)
