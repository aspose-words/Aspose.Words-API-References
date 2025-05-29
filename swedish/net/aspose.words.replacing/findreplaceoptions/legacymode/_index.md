---
title: FindReplaceOptions.LegacyMode
linktitle: LegacyMode
articleTitle: LegacyMode
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FindReplaceOptions LegacyMode för att enkelt växla mellan den klassiska sök/ersätt-algoritmen för förbättrad funktionalitet och en smidig användarupplevelse.
type: docs
weight: 130
url: /sv/net/aspose.words.replacing/findreplaceoptions/legacymode/
---
## FindReplaceOptions.LegacyMode property

Hämtar eller ställer in ett booleskt värde som indikerar att den gamla sök/ersätt-algoritmen används.

```csharp
public bool LegacyMode { get; set; }
```

## Anmärkningar

Använd den här flaggan om du behöver exakt samma beteende som innan den avancerade sök-/ersätt-funktionen introducerades. Observera att den gamla algoritmen inte stöder avancerade funktioner som att ersätta med brytningar, tillämpa formatering och så vidare.

## Exempel

Visar hur man känner igen och använder substitutioner inom ersättningsmönster.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Jason gave money to Paul.");

Regex regex = new Regex(@"([A-z]+) gave money to ([A-z]+)");

FindReplaceOptions options = new FindReplaceOptions();
options.UseSubstitutions = true;

// Att använda äldre läge har inte stöd för många avancerade funktioner, så vi måste ställa in det på 'false'.
options.LegacyMode = false;

doc.Range.Replace(regex, @"$2 took money from $1", options);

Assert.AreEqual(doc.GetText(), "Paul took money from Jason.\f");
```

### Se även

* class [FindReplaceOptions](../)
* namnutrymme [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../../)
