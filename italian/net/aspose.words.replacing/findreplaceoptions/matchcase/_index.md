---
title: FindReplaceOptions.MatchCase
linktitle: MatchCase
articleTitle: MatchCase
second_title: Aspose.Words per .NET
description: Scopri la proprietà MatchCase in FindReplaceOptions, abilita confronti con o senza distinzione tra maiuscole e minuscole per una modifica precisa del testo. Ottimizza il tuo flusso di lavoro!
type: docs
weight: 140
url: /it/net/aspose.words.replacing/findreplaceoptions/matchcase/
---
## FindReplaceOptions.MatchCase property

Vero indica un confronto con distinzione tra maiuscole e minuscole, falso indica un confronto senza distinzione tra maiuscole e minuscole.

```csharp
public bool MatchCase { get; set; }
```

## Esempi

Mostra come attivare o disattivare la distinzione tra maiuscole e minuscole quando si esegue un'operazione di ricerca e sostituzione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
FindReplaceOptions options = new FindReplaceOptions();

// Imposta il flag "MatchCase" su "true" per applicare la distinzione tra maiuscole e minuscole durante la ricerca delle stringhe da sostituire.
// Impostare il flag "MatchCase" su "false" per ignorare la distinzione tra maiuscole e minuscole durante la ricerca del testo da sostituire.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

### Guarda anche

* class [FindReplaceOptions](../)
* spazio dei nomi [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assemblea [Aspose.Words](../../../)
