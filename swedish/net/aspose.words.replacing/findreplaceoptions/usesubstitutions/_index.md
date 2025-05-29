---
title: FindReplaceOptions.UseSubstitutions
linktitle: UseSubstitutions
articleTitle: UseSubstitutions
second_title: Aspose.Words för .NET
description: Upptäck egenskapen UseSubstitutions i FindReplaceOptions. Aktivera enkelt substitutioner i ersättningsmönster för förbättrad flexibilitet vid textredigering.
type: docs
weight: 190
url: /sv/net/aspose.words.replacing/findreplaceoptions/usesubstitutions/
---
## FindReplaceOptions.UseSubstitutions property

Hämtar eller ställer in ett booleskt värde som anger om substitutioner inom ersättningsmönster ska kännas igen och användas. Standardvärdet är`falsk` .

```csharp
public bool UseSubstitutions { get; set; }
```

## Anmärkningar

För detaljer om substitutionselement, se: https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

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

Visar hur man ersätter texten med substitutioner.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("John sold a car to Paul.");
builder.Writeln("Jane sold a house to Joe.");

// Vi kan använda ett "FindReplaceOptions"-objekt för att modifiera sök-och-ersätt-processen.
FindReplaceOptions options = new FindReplaceOptions();

// Sätt egenskapen "UseSubstitutions" till "true" för att få
// sök-och-ersätt-operationen för att känna igen substitutionselement.
// Sätt egenskapen "UseSubstitutions" till "false" för att ignorera substitutionselement.
options.UseSubstitutions = useSubstitutions;

Regex regex = new Regex(@"([A-z]+) sold a ([A-z]+) to ([A-z]+)");
doc.Range.Replace(regex, @"$3 bought a $2 from $1", options);

Assert.AreEqual(
    useSubstitutions
        ? "Paul bought a car from John.\rJoe bought a house from Jane."
        : "$3 bought a $2 from $1.\r$3 bought a $2 from $1.", doc.GetText().Trim());
```

### Se även

* class [FindReplaceOptions](../)
* namnutrymme [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../../)
