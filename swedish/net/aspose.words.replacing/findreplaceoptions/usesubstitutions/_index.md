---
title: FindReplaceOptions.UseSubstitutions
second_title: Aspose.Words för .NET API Referens
description: FindReplaceOptions fast egendom. Hämtar eller ställer in ett booleskt värde som indikerar om ersättningar ska identifieras och användas inom ersättningsmönster. Standardvärdet ärfalsk .
type: docs
weight: 180
url: /sv/net/aspose.words.replacing/findreplaceoptions/usesubstitutions/
---
## FindReplaceOptions.UseSubstitutions property

Hämtar eller ställer in ett booleskt värde som indikerar om ersättningar ska identifieras och användas inom ersättningsmönster. Standardvärdet är`falsk` .

```csharp
public bool UseSubstitutions { get; set; }
```

### Anmärkningar

För detaljer om substitutionselement, se: https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

### Exempel

Visar hur man känner igen och använder ersättningar inom ersättningsmönster.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Jason gave money to Paul.");

Regex regex = new Regex(@"([A-z]+) gave money to ([A-z]+)");

FindReplaceOptions options = new FindReplaceOptions();
options.UseSubstitutions = true;

// Att använda äldre läge stöder inte många avancerade funktioner, så vi måste ställa in det på "false".
options.LegacyMode = false;

doc.Range.Replace(regex, @"$2 took money from $1", options);

Assert.AreEqual(doc.GetText(), "Paul took money from Jason.\f");
```

Visar hur man ersätter texten med ersättningar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("John sold a car to Paul.");
builder.Writeln("Jane sold a house to Joe.");

// Vi kan använda ett "FindReplaceOptions"-objekt för att ändra sök-och-ersätt-processen.
FindReplaceOptions options = new FindReplaceOptions();

// Ställ in egenskapen "UseSubstitutions" till "true" för att få
// hitta-och-ersätt-operationen för att känna igen substitutionselement.
// Ställ in egenskapen "UseSubstitutions" till "false" för att ignorera substitutionselement.
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
* namnutrymme [Aspose.Words.Replacing](../../findreplaceoptions/)
* hopsättning [Aspose.Words](../../../)


