---
title: FindReplaceOptions.UseSubstitutions
linktitle: UseSubstitutions
articleTitle: UseSubstitutions
second_title: Aspose.Words für .NET
description: FindReplaceOptions UseSubstitutions eigendom. Ruft einen booleschen Wert ab der angibt ob Ersetzungen innerhalb von Ersetzungsmustern erkannt und verwendet werden sollen oder legt diesen fest. Der Standardwert istFALSCH  in C#.
type: docs
weight: 180
url: /de/net/aspose.words.replacing/findreplaceoptions/usesubstitutions/
---
## FindReplaceOptions.UseSubstitutions property

Ruft einen booleschen Wert ab, der angibt, ob Ersetzungen innerhalb von Ersetzungsmustern erkannt und verwendet werden sollen, oder legt diesen fest. Der Standardwert ist`FALSCH` .

```csharp
public bool UseSubstitutions { get; set; }
```

## Bemerkungen

Einzelheiten zu Substitutionselementen finden Sie unter: https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

## Beispiele

Zeigt, wie Ersetzungen innerhalb von Ersetzungsmustern erkannt und verwendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Jason gave money to Paul.");

Regex regex = new Regex(@"([A-z]+) gave money to ([A-z]+)");

FindReplaceOptions options = new FindReplaceOptions();
options.UseSubstitutions = true;

// Die Verwendung des Legacy-Modus unterstützt viele erweiterte Funktionen nicht, daher müssen wir ihn auf „false“ setzen.
options.LegacyMode = false;

doc.Range.Replace(regex, @"$2 took money from $1", options);

Assert.AreEqual(doc.GetText(), "Paul took money from Jason.\f");
```

Zeigt, wie der Text durch Ersetzungen ersetzt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("John sold a car to Paul.");
builder.Writeln("Jane sold a house to Joe.");

// Wir können ein „FindReplaceOptions“-Objekt verwenden, um den Such- und Ersetzungsprozess zu ändern.
FindReplaceOptions options = new FindReplaceOptions();

// Setzen Sie die Eigenschaft „UseSubstitutions“ auf „true“, um sie abzurufen
// die Such- und Ersetzungsoperation zum Erkennen von Substitutionselementen.
// Setzen Sie die Eigenschaft „UseSubstitutions“ auf „false“, um Substitutionselemente zu ignorieren.
options.UseSubstitutions = useSubstitutions;

Regex regex = new Regex(@"([A-z]+) sold a ([A-z]+) to ([A-z]+)");
doc.Range.Replace(regex, @"$3 bought a $2 from $1", options);

Assert.AreEqual(
    useSubstitutions
        ? "Paul bought a car from John.\rJoe bought a house from Jane."
        : "$3 bought a $2 from $1.\r$3 bought a $2 from $1.", doc.GetText().Trim());
```

### Siehe auch

* class [FindReplaceOptions](../)
* namensraum [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Montage [Aspose.Words](../../../)
