---
title: FindReplaceOptions.IgnoreDeleted
linktitle: IgnoreDeleted
articleTitle: IgnoreDeleted
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FindReplaceOptions IgnoreDeleted, styr textens synlighet i borttagna versioner med en enkel booleskt knapp. Förbättra din redigeringsupplevelse!
type: docs
weight: 60
url: /sv/net/aspose.words.replacing/findreplaceoptions/ignoredeleted/
---
## FindReplaceOptions.IgnoreDeleted property

Hämtar eller ställer in ett booleskt värde som anger att text i borttagna revisioner ska ignoreras. Standardvärdet är`falsk` .

```csharp
public bool IgnoreDeleted { get; set; }
```

## Exempel

Visar hur man inkluderar eller ignorerar text i borttagningsversioner under en sök-och-ersätt-åtgärd.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Börja spåra revisioner och ta bort det andra stycket, vilket skapar en borttagningsrevision.
// Det stycket kommer att finnas kvar i dokumentet tills vi accepterar borttagningsrevisionen.
doc.StartTrackRevisions("John Doe", DateTime.Now);
doc.FirstSection.Body.Paragraphs[1].Remove();
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsDeleteRevision);

// Vi kan använda ett "FindReplaceOptions"-objekt för att modifiera sök- och ersättningsprocessen.
FindReplaceOptions options = new FindReplaceOptions();

// Sätt flaggan "IgnoreDeleted" till "true" för att få sök-och-ersätt-funktionen
// operation för att ignorera stycken som är borttagningsrevisioner.
// Sätt flaggan "IgnoreDeleted" till "false" för att få sök-och-ersätt-funktionen
// operation för att även söka efter text inuti borttagningsversioner.
options.IgnoreDeleted = ignoreTextInsideDeleteRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideDeleteRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### Se även

* class [FindReplaceOptions](../)
* namnutrymme [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../../)
