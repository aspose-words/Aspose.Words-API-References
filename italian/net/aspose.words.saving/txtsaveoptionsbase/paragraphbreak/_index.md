---
title: TxtSaveOptionsBase.ParagraphBreak
second_title: Aspose.Words per .NET API Reference
description: TxtSaveOptionsBase proprietà. Specifica la stringa da utilizzare come interruzione di paragrafo durante lesportazione in formati di testo.
type: docs
weight: 40
url: /it/net/aspose.words.saving/txtsaveoptionsbase/paragraphbreak/
---
## TxtSaveOptionsBase.ParagraphBreak property

Specifica la stringa da utilizzare come interruzione di paragrafo durante l'esportazione in formati di testo.

```csharp
public string ParagraphBreak { get; set; }
```

### Osservazioni

Il valore predefinito è[`CrLf`](../../../aspose.words/controlchar/crlf/).

### Esempi

Mostra come salvare un documento .txt con un'interruzione di paragrafo personalizzata.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");
builder.Write("Paragraph 3.");

// Crea un oggetto "TxtSaveOptions", che possiamo passare al metodo "Save" del documento
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

* class [TxtSaveOptionsBase](../)
* spazio dei nomi [Aspose.Words.Saving](../../txtsaveoptionsbase/)
* assemblea [Aspose.Words](../../../)


