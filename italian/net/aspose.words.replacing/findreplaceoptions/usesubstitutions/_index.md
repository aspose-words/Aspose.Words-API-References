---
title: FindReplaceOptions.UseSubstitutions
linktitle: UseSubstitutions
articleTitle: UseSubstitutions
second_title: Aspose.Words per .NET
description: Scopri la proprietà UseSubstitutions in FindReplaceOptions. Abilita facilmente le sostituzioni nei modelli di sostituzione per una maggiore flessibilità nella modifica del testo.
type: docs
weight: 190
url: /it/net/aspose.words.replacing/findreplaceoptions/usesubstitutions/
---
## FindReplaceOptions.UseSubstitutions property

Ottiene o imposta un valore booleano che indica se riconoscere e utilizzare le sostituzioni all'interno dei modelli di sostituzione. Il valore predefinito è`falso` .

```csharp
public bool UseSubstitutions { get; set; }
```

## Osservazioni

Per i dettagli sugli elementi di sostituzione, fare riferimento a: https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

## Esempi

Mostra come riconoscere e utilizzare le sostituzioni all'interno dei modelli di sostituzione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Jason gave money to Paul.");

Regex regex = new Regex(@"([A-z]+) gave money to ([A-z]+)");

FindReplaceOptions options = new FindReplaceOptions();
options.UseSubstitutions = true;

// L'utilizzo della modalità legacy non supporta molte funzionalità avanzate, quindi dobbiamo impostarla su "false".
options.LegacyMode = false;

doc.Range.Replace(regex, @"$2 took money from $1", options);

Assert.AreEqual(doc.GetText(), "Paul took money from Jason.\f");
```

Mostra come sostituire il testo con delle sostituzioni.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("John sold a car to Paul.");
builder.Writeln("Jane sold a house to Joe.");

// Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
FindReplaceOptions options = new FindReplaceOptions();

// Imposta la proprietà "UseSubstitutions" su "true" per ottenere
// l'operazione di ricerca e sostituzione per riconoscere gli elementi di sostituzione.
// Impostare la proprietà "UseSubstitutions" su "false" per ignorare gli elementi di sostituzione.
options.UseSubstitutions = useSubstitutions;

Regex regex = new Regex(@"([A-z]+) sold a ([A-z]+) to ([A-z]+)");
doc.Range.Replace(regex, @"$3 bought a $2 from $1", options);

Assert.AreEqual(
    useSubstitutions
        ? "Paul bought a car from John.\rJoe bought a house from Jane."
        : "$3 bought a $2 from $1.\r$3 bought a $2 from $1.", doc.GetText().Trim());
```

### Guarda anche

* class [FindReplaceOptions](../)
* spazio dei nomi [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assemblea [Aspose.Words](../../../)
