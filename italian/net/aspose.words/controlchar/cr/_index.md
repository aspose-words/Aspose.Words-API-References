---
title: ControlChar.Cr
linktitle: Cr
articleTitle: Cr
second_title: Aspose.Words per .NET
description: ControlChar Cr campo. Carattere di ritorno a capo x000d o r. Uguale aParagraphBreak  in C#.
type: docs
weight: 50
url: /it/net/aspose.words/controlchar/cr/
---
## ControlChar.Cr field

Carattere di ritorno a capo: "\x000d" o "\r". Uguale a[`ParagraphBreak`](../paragraphbreak/) .

```csharp
public static readonly string Cr;
```

## Esempi

Mostra come utilizzare i caratteri di controllo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci paragrafi con testo con DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// La conversione del documento in formato testo rivela i caratteri di controllo
// rappresenta alcuni degli elementi strutturali del documento, come le interruzioni di pagina.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// Quando si converte un documento in formato stringa,
// possiamo omettere alcuni caratteri di controllo con il metodo Trim.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### Guarda anche

* class [ControlChar](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
