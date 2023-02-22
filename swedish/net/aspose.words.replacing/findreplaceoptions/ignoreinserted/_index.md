---
title: FindReplaceOptions.IgnoreInserted
second_title: Aspose.Words för .NET API Referens
description: FindReplaceOptions fast egendom. Hämtar eller ställer in ett booleskt värde som indikerar att texten i infogningsversioner ska ignoreras. Standardvärdet ärfalsk .
type: docs
weight: 100
url: /sv/net/aspose.words.replacing/findreplaceoptions/ignoreinserted/
---
## FindReplaceOptions.IgnoreInserted property

Hämtar eller ställer in ett booleskt värde som indikerar att texten i infogningsversioner ska ignoreras. Standardvärdet är`falsk` .

```csharp
public bool IgnoreInserted { get; set; }
```

### Exempel

Visar hur man inkluderar eller ignorerar text i infogningsversioner under en sök-och-ersätt-operation.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Börja spåra revisioner och infoga ett stycke. Det stycket kommer att vara en insättningsrevision.
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("Hello again!");
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsInsertRevision);

// Vi kan använda ett "FindReplaceOptions"-objekt för att ändra sök-och-ersätt-processen.
FindReplaceOptions options = new FindReplaceOptions();

// Ställ in flaggan "IgnoreInserted" till "true" för att få sök-och-ersätt
// operation för att ignorera stycken som är insert revisioner.
// Sätt flaggan "IgnoreInserted" till "false" för att få sök-och-ersätt
// operation för att även söka efter text i infoga versioner.
options.IgnoreInserted = ignoreTextInsideInsertRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideInsertRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### Se även

* class [FindReplaceOptions](../)
* namnutrymme [Aspose.Words.Replacing](../../findreplaceoptions/)
* hopsättning [Aspose.Words](../../../)


