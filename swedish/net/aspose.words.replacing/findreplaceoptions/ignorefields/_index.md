---
title: FindReplaceOptions.IgnoreFields
linktitle: IgnoreFields
articleTitle: IgnoreFields
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FindReplaceOptions IgnoreFields för att enkelt hantera text i fält. Kontrollera när innehåll ska ignoreras för effektiv sökning!
type: docs
weight: 80
url: /sv/net/aspose.words.replacing/findreplaceoptions/ignorefields/
---
## FindReplaceOptions.IgnoreFields property

Hämtar eller ställer in ett booleskt värde som anger att text i fält ska ignoreras. Standardvärdet är`falsk` .

```csharp
public bool IgnoreFields { get; set; }
```

## Anmärkningar

Det här alternativet påverkar hela fältet (alla noder mellan FieldStart ochFieldEnd).

För att endast ignorera fältkoder, använd motsvarande alternativ[`IgnoreFieldCodes`](../ignorefieldcodes/).

## Exempel

Visar hur man ignorerar text inuti fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertField("QUOTE", "Hello again!");

// Vi kan använda ett "FindReplaceOptions"-objekt för att modifiera sök-och-ersätt-processen.
FindReplaceOptions options = new FindReplaceOptions();

// Sätt flaggan "IgnoreFields" till "true" för att få sök-och-ersätt-funktionen
// operation för att ignorera text inuti fält.
// Sätt flaggan "IgnoreFields" till "false" för att få sök-och-ersätt-funktionen
// operation för att även söka efter text inuti fält.
options.IgnoreFields = ignoreTextInsideFields;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideFields
        ? "Greetings world!\r\u0013QUOTE\u0014Hello again!\u0015"
        : "Greetings world!\r\u0013QUOTE\u0014Greetings again!\u0015", doc.GetText().Trim());
```

### Se även

* class [FindReplaceOptions](../)
* namnutrymme [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../../)
