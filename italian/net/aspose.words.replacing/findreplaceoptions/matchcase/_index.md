---
title: MatchCase
second_title: Aspose.Words per .NET API Reference
description: True indica il confronto con distinzione tra maiuscole e minuscole false indica un confronto senza distinzione tra maiuscole e minuscole.
type: docs
weight: 120
url: /it/net/aspose.words.replacing/findreplaceoptions/matchcase/
---
## FindReplaceOptions.MatchCase property

True indica il confronto con distinzione tra maiuscole e minuscole, false indica un confronto senza distinzione tra maiuscole e minuscole.

```csharp
public bool MatchCase { get; set; }
```

### Esempi

Mostra come attivare la distinzione tra maiuscole e minuscole durante l'esecuzione di un'operazione di ricerca e sostituzione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Possiamo usare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
FindReplaceOptions options = new FindReplaceOptions();

// Imposta il flag "MatchCase" su "true" per applicare la distinzione tra maiuscole e minuscole mentre trovi le stringhe da sostituire.
// Imposta il flag "MatchCase" su "false" per ignorare il carattere maiuscolo durante la ricerca del testo da sostituire.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

### Guarda anche

* class [FindReplaceOptions](../../findreplaceoptions)
* spazio dei nomi [Aspose.Words.Replacing](../../findreplaceoptions)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
