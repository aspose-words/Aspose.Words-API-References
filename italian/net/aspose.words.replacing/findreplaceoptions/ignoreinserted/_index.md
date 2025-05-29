---
title: FindReplaceOptions.IgnoreInserted
linktitle: IgnoreInserted
articleTitle: IgnoreInserted
second_title: Aspose.Words per .NET
description: Scopri la proprietà IgnoreInserted di FindReplaceOptions e controlla la gestione del testo nelle revisioni di inserimento con questa semplice impostazione booleana. Il valore predefinito è "false".
type: docs
weight: 100
url: /it/net/aspose.words.replacing/findreplaceoptions/ignoreinserted/
---
## FindReplaceOptions.IgnoreInserted property

Ottiene o imposta un valore booleano che indica di ignorare il testo all'interno delle revisioni di inserimento. Il valore predefinito è`falso` .

```csharp
public bool IgnoreInserted { get; set; }
```

## Esempi

Mostra come includere o ignorare il testo all'interno delle revisioni di inserimento durante un'operazione di ricerca e sostituzione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Inizia a monitorare le revisioni e inserisci un paragrafo. Quel paragrafo sarà una revisione inserita.
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("Hello again!");
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsInsertRevision);

// Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
FindReplaceOptions options = new FindReplaceOptions();

// Imposta il flag "IgnoreInserted" su "true" per ottenere la funzione di ricerca e sostituzione
// operazione per ignorare i paragrafi che sono revisioni inserite.
// Imposta il flag "IgnoreInserted" su "false" per ottenere la funzione di ricerca e sostituzione
// operazione per cercare anche il testo all'interno delle revisioni inserite.
options.IgnoreInserted = ignoreTextInsideInsertRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideInsertRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### Guarda anche

* class [FindReplaceOptions](../)
* spazio dei nomi [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assemblea [Aspose.Words](../../../)
