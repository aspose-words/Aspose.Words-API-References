---
title: TxtSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words per .NET
description: Scopri come la proprietà SaveFormat di TxtSaveOptions definisce i formati di salvataggio dei documenti, garantendo che i file siano sempre nel formato di testo preferito.
type: docs
weight: 60
url: /it/net/aspose.words.saving/txtsaveoptions/saveformat/
---
## TxtSaveOptions.SaveFormat property

Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere soloText .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Esempi

Mostra come salvare un documento .txt con un'interruzione di paragrafo personalizzata.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");
builder.Write("Paragraph 3.");

// Creiamo un oggetto "TxtSaveOptions", che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui salviamo il documento in testo normale.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

Assert.AreEqual(SaveFormat.Text, txtSaveOptions.SaveFormat);

// Imposta "ParagraphBreak" su un valore personalizzato che desideriamo inserire alla fine di ogni paragrafo.
txtSaveOptions.ParagraphBreak = " End of paragraph.\n\n\t";

doc.Save(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt");

Assert.AreEqual("Paragraph 1. End of paragraph.\n\n\t" +
                "Paragraph 2. End of paragraph.\n\n\t" +
                "Paragraph 3. End of paragraph.\n\n\t", docText);
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [TxtSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
