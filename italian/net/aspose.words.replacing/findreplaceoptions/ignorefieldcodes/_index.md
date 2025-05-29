---
title: FindReplaceOptions.IgnoreFieldCodes
linktitle: IgnoreFieldCodes
articleTitle: IgnoreFieldCodes
second_title: Aspose.Words per .NET
description: Scopri la proprietà IgnoreFieldCodes di FindReplaceOptions per gestire facilmente il testo nei codici di campo. Controlla la visibilità con una semplice impostazione booleana!
type: docs
weight: 70
url: /it/net/aspose.words.replacing/findreplaceoptions/ignorefieldcodes/
---
## FindReplaceOptions.IgnoreFieldCodes property

Ottiene o imposta un valore booleano che indica di ignorare il testo all'interno dei codici di campo. Il valore predefinito è`falso` .

```csharp
public bool IgnoreFieldCodes { get; set; }
```

## Osservazioni

Questa opzione riguarda solo i codici di campo (non ignora i nodi tra FieldSeparator EFieldEnd).

Per ignorare l'intero campo, utilizzare l'opzione corrispondente[`IgnoreFields`](../ignorefields/).

## Esempi

Mostra come ignorare il testo all'interno dei codici di campo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField("INCLUDETEXT", "Test IT!");

FindReplaceOptions options = new FindReplaceOptions {IgnoreFieldCodes = ignoreFieldCodes};

// Sostituisci 'T' nel documento ignorando o meno il testo all'interno del codice di campo.
doc.Range.Replace(new Regex("T"), "*", options);
Console.WriteLine(doc.GetText());

Assert.AreEqual(
    ignoreFieldCodes
        ? "\u0013INCLUDETEXT\u0014*est I*!\u0015"
        : "\u0013INCLUDE*EX*\u0014*est I*!\u0015", doc.GetText().Trim());
```

### Guarda anche

* class [FindReplaceOptions](../)
* spazio dei nomi [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assemblea [Aspose.Words](../../../)
