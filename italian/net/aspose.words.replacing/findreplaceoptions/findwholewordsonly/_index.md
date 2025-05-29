---
title: FindReplaceOptions.FindWholeWordsOnly
linktitle: FindWholeWordsOnly
articleTitle: FindWholeWordsOnly
second_title: Aspose.Words per .NET
description: Scopri come la proprietà FindWholeWordsOnly migliora la tua ricerca con risultati accurati, garantendo che oldValue corrisponda solo a una parola a sé stante.
type: docs
weight: 50
url: /it/net/aspose.words.replacing/findreplaceoptions/findwholewordsonly/
---
## FindReplaceOptions.FindWholeWordsOnly property

True indica che oldValue deve essere una parola autonoma.

```csharp
public bool FindWholeWordsOnly { get; set; }
```

## Esempi

Mostra come attivare o disattivare operazioni di ricerca e sostituzione autonome di sole parole.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
FindReplaceOptions options = new FindReplaceOptions();

// Imposta il flag "FindWholeWordsOnly" su "true" per sostituire il testo trovato se non fa parte di un'altra parola.
// Imposta il flag "FindWholeWordsOnly" su "false" per sostituire tutto il testo, indipendentemente da ciò che lo circonda.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### Guarda anche

* class [FindReplaceOptions](../)
* spazio dei nomi [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assemblea [Aspose.Words](../../../)
