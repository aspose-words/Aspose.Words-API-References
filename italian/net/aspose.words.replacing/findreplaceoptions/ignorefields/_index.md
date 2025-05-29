---
title: FindReplaceOptions.IgnoreFields
linktitle: IgnoreFields
articleTitle: IgnoreFields
second_title: Aspose.Words per .NET
description: Scopri la proprietà IgnoreFields di FindReplaceOptions per gestire facilmente il testo all'interno dei campi. Controlla quando ignorare il contenuto per una ricerca efficiente!
type: docs
weight: 80
url: /it/net/aspose.words.replacing/findreplaceoptions/ignorefields/
---
## FindReplaceOptions.IgnoreFields property

Ottiene o imposta un valore booleano che indica di ignorare il testo all'interno dei campi. Il valore predefinito è`falso` .

```csharp
public bool IgnoreFields { get; set; }
```

## Osservazioni

Questa opzione interessa l'intero campo (tutti i nodi tra FieldStart EFieldEnd).

Per ignorare solo i codici di campo, utilizzare l'opzione corrispondente[`IgnoreFieldCodes`](../ignorefieldcodes/).

## Esempi

Mostra come ignorare il testo all'interno dei campi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertField("QUOTE", "Hello again!");

// Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
FindReplaceOptions options = new FindReplaceOptions();

// Imposta il flag "IgnoreFields" su "true" per ottenere la funzione di ricerca e sostituzione
// operazione per ignorare il testo all'interno dei campi.
// Imposta il flag "IgnoreFields" su "false" per ottenere la funzione di ricerca e sostituzione
// operazione per cercare anche il testo all'interno dei campi.
options.IgnoreFields = ignoreTextInsideFields;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideFields
        ? "Greetings world!\r\u0013QUOTE\u0014Hello again!\u0015"
        : "Greetings world!\r\u0013QUOTE\u0014Greetings again!\u0015", doc.GetText().Trim());
```

### Guarda anche

* class [FindReplaceOptions](../)
* spazio dei nomi [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assemblea [Aspose.Words](../../../)
