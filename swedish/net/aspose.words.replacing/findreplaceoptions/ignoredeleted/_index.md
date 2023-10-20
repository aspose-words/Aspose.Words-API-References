---
title: FindReplaceOptions.IgnoreDeleted
linktitle: IgnoreDeleted
articleTitle: IgnoreDeleted
second_title: Aspose.Words för .NET
description: FindReplaceOptions IgnoreDeleted fast egendom. Hämtar eller ställer in ett booleskt värde som anger att texten i raderingsversioner ska ignoreras. Standardvärdet ärfalsk  i C#.
type: docs
weight: 60
url: /sv/net/aspose.words.replacing/findreplaceoptions/ignoredeleted/
---
## FindReplaceOptions.IgnoreDeleted property

Hämtar eller ställer in ett booleskt värde som anger att texten i raderingsversioner ska ignoreras. Standardvärdet är`falsk` .

```csharp
public bool IgnoreDeleted { get; set; }
```

## Exempel

Visar hur man inkluderar eller ignorerar text i raderingsversioner under en sök-och-ersätt-operation.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Börja spåra revisioner och ta bort det andra stycket, vilket skapar en raderingsrevision.
// Det stycket kommer att finnas kvar i dokumentet tills vi accepterar raderingsrevisionen.
doc.StartTrackRevisions("John Doe", DateTime.Now);
doc.FirstSection.Body.Paragraphs[1].Remove();
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsDeleteRevision);

// Vi kan använda ett "FindReplaceOptions"-objekt för att ändra sök- och ersätt-processen.
FindReplaceOptions options = new FindReplaceOptions();

// Sätt flaggan "IgnoreDeleted" till "true" för att få sök-och-ersätt
// operation för att ignorera stycken som är raderingsrevisioner.
// Sätt flaggan "IgnoreDeleted" till "false" för att få sök-och-ersätt
// operation för att även söka efter text i raderingsversioner.
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
