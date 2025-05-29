---
title: ImportFormatOptions.AdjustSentenceAndWordSpacing
linktitle: AdjustSentenceAndWordSpacing
articleTitle: AdjustSentenceAndWordSpacing
second_title: Aspose.Words per .NET
description: Scopri la proprietà AdjustSentenceAndWordSpacing di ImportFormatOptions. Controlla facilmente la spaziatura automatica di frasi e parole per una migliore chiarezza del testo.
type: docs
weight: 20
url: /it/net/aspose.words/importformatoptions/adjustsentenceandwordspacing/
---
## ImportFormatOptions.AdjustSentenceAndWordSpacing property

Ottiene o imposta un valore booleano che specifica se regolare automaticamente la spaziatura delle frasi e delle parole. Il valore predefinito è`falso` .

```csharp
public bool AdjustSentenceAndWordSpacing { get; set; }
```

## Esempi

Mostra come regolare automaticamente la spaziatura delle frasi e delle parole.

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

DocumentBuilder builder = new DocumentBuilder(srcDoc);
builder.Write("Dolor sit amet.");

builder = new DocumentBuilder(dstDoc);
builder.Write("Lorem ipsum.");

ImportFormatOptions options = new ImportFormatOptions() { AdjustSentenceAndWordSpacing = true };
builder.InsertDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

Assert.AreEqual("Lorem ipsum. Dolor sit amet.", dstDoc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Guarda anche

* class [ImportFormatOptions](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
