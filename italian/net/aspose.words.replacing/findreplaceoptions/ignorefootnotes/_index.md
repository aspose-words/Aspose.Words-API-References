---
title: FindReplaceOptions.IgnoreFootnotes
linktitle: IgnoreFootnotes
articleTitle: IgnoreFootnotes
second_title: Aspose.Words per .NET
description: Scopri la proprietà FindReplaceOptions IgnoreFootnotes per gestire facilmente le note a piè di pagina nei tuoi documenti. Migliora l'efficienza di editing con questa semplice opzione!
type: docs
weight: 90
url: /it/net/aspose.words.replacing/findreplaceoptions/ignorefootnotes/
---
## FindReplaceOptions.IgnoreFootnotes property

Ottiene o imposta un valore booleano che indica di ignorare le note a piè di pagina. Il valore predefinito è`falso` .

```csharp
public bool IgnoreFootnotes { get; set; }
```

## Esempi

Mostra come ignorare le note a piè di pagina durante un'operazione di ricerca e sostituzione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Footnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder.InsertParagraph();

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Endnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// Imposta il flag "IgnoreFootnotes" su "true" per ottenere la funzione di ricerca e sostituzione
// operazione per ignorare il testo all'interno delle note a piè di pagina.
// Imposta il flag "IgnoreFootnotes" su "false" per ottenere la funzione di ricerca e sostituzione
// operazione per cercare anche il testo all'interno delle note a piè di pagina.
FindReplaceOptions options = new FindReplaceOptions { IgnoreFootnotes = isIgnoreFootnotes };
doc.Range.Replace("Lorem ipsum", "Replaced Lorem ipsum", options);
```

### Guarda anche

* class [FindReplaceOptions](../)
* spazio dei nomi [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assemblea [Aspose.Words](../../../)
