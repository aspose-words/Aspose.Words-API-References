---
title: FindReplaceOptions.IgnoreFields
second_title: Aspose.Words per .NET API Reference
description: FindReplaceOptions proprietà. Ottiene o imposta un valore booleano che indica di ignorare il testo allinterno dei campi. Il valore predefinito èfalso .
type: docs
weight: 80
url: /it/net/aspose.words.replacing/findreplaceoptions/ignorefields/
---
## FindReplaceOptions.IgnoreFields property

Ottiene o imposta un valore booleano che indica di ignorare il testo all'interno dei campi. Il valore predefinito è`falso` .

```csharp
public bool IgnoreFields { get; set; }
```

### Osservazioni

Questa opzione influisce sull'intero campo (tutti i nodi tra FieldStart EFieldEnd).

Per ignorare solo i codici di campo, utilizzare l'opzione corrispondente[`IgnoreFieldCodes`](../ignorefieldcodes/).

### Esempi

Mostra come ignorare il testo all'interno dei campi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertField("QUOTE", "Hello again!");

// Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
FindReplaceOptions options = new FindReplaceOptions();

// Imposta il flag "IgnoreFields" su "true" per ottenere la ricerca e sostituzione
// operazione per ignorare il testo all'interno dei campi.
// Imposta il flag "IgnoreFields" su "false" per ottenere la ricerca e sostituzione
// operazione per cercare anche testo all'interno dei campi.
options.IgnoreFields = ignoreTextInsideFields;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideFields
        ? "Greetings world!\r\u0013QUOTE\u0014Hello again!\u0015"
        : "Greetings world!\r\u0013QUOTE\u0014Greetings again!\u0015", doc.GetText().Trim());
```

### Guarda anche

* class [FindReplaceOptions](../)
* spazio dei nomi [Aspose.Words.Replacing](../../findreplaceoptions/)
* assemblea [Aspose.Words](../../../)


