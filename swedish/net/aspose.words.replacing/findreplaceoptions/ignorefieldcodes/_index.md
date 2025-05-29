---
title: FindReplaceOptions.IgnoreFieldCodes
linktitle: IgnoreFieldCodes
articleTitle: IgnoreFieldCodes
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FindReplaceOptions IgnoreFieldCodes för att enkelt hantera text i fältkoder. Kontrollera synligheten med en enkel boolesk inställning!
type: docs
weight: 70
url: /sv/net/aspose.words.replacing/findreplaceoptions/ignorefieldcodes/
---
## FindReplaceOptions.IgnoreFieldCodes property

Hämtar eller ställer in ett booleskt värde som anger att text i fältkoder ska ignoreras. Standardvärdet är`falsk` .

```csharp
public bool IgnoreFieldCodes { get; set; }
```

## Anmärkningar

Det här alternativet påverkar endast fältkoder (det ignorerar inte noder mellan FieldSeparator ochFieldEnd).

För att ignorera hela fältet, använd motsvarande alternativ[`IgnoreFields`](../ignorefields/).

## Exempel

Visar hur man ignorerar text inuti fältkoder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField("INCLUDETEXT", "Test IT!");

FindReplaceOptions options = new FindReplaceOptions {IgnoreFieldCodes = ignoreFieldCodes};

// Ersätt 'T' i dokumentet, ignorerar text inuti fältkod eller inte.
doc.Range.Replace(new Regex("T"), "*", options);
Console.WriteLine(doc.GetText());

Assert.AreEqual(
    ignoreFieldCodes
        ? "\u0013INCLUDETEXT\u0014*est I*!\u0015"
        : "\u0013INCLUDE*EX*\u0014*est I*!\u0015", doc.GetText().Trim());
```

### Se även

* class [FindReplaceOptions](../)
* namnutrymme [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../../)
