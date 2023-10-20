---
title: FindReplaceOptions.IgnoreDeleted
linktitle: IgnoreDeleted
articleTitle: IgnoreDeleted
second_title: Aspose.Words per .NET
description: FindReplaceOptions IgnoreDeleted proprietà. Ottiene o imposta un valore booleano che indica di ignorare il testo allinterno delle revisioni di eliminazione. Il valore predefinito èfalso  in C#.
type: docs
weight: 60
url: /it/net/aspose.words.replacing/findreplaceoptions/ignoredeleted/
---
## FindReplaceOptions.IgnoreDeleted property

Ottiene o imposta un valore booleano che indica di ignorare il testo all'interno delle revisioni di eliminazione. Il valore predefinito è`falso` .

```csharp
public bool IgnoreDeleted { get; set; }
```

## Esempi

Mostra come includere o ignorare il testo all'interno delle revisioni di eliminazione durante un'operazione di ricerca e sostituzione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Inizia a tenere traccia delle revisioni e rimuove il secondo paragrafo, che creerà una revisione di eliminazione.
// Quel paragrafo persisterà nel documento finché non accetteremo la revisione di eliminazione.
doc.StartTrackRevisions("John Doe", DateTime.Now);
doc.FirstSection.Body.Paragraphs[1].Remove();
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsDeleteRevision);

// Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
FindReplaceOptions options = new FindReplaceOptions();

// Imposta il flag "IgnoreDeleted" su "true" per ottenere la ricerca e sostituzione
// operazione per ignorare i paragrafi che eliminano le revisioni.
// Imposta il flag "IgnoreDeleted" su "false" per ottenere la ricerca e sostituzione
// operazione per cercare anche il testo all'interno delle revisioni di eliminazione.
options.IgnoreDeleted = ignoreTextInsideDeleteRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideDeleteRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### Guarda anche

* class [FindReplaceOptions](../)
* spazio dei nomi [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assemblea [Aspose.Words](../../../)
