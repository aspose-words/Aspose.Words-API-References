---
title: ImportFormatOptions.IgnoreTextBoxes
linktitle: IgnoreTextBoxes
articleTitle: IgnoreTextBoxes
second_title: Aspose.Words per .NET
description: Scopri come la proprietà IgnoreTextBoxes di ImportFormatOptions migliora la formattazione dei tuoi documenti controllando il contenuto delle caselle di testo. Ottimizza con facilità oggi stesso!
type: docs
weight: 50
url: /it/net/aspose.words/importformatoptions/ignoretextboxes/
---
## ImportFormatOptions.IgnoreTextBoxes property

Ottiene o imposta un valore booleano che specifica che la formattazione di origine del contenuto delle caselle di testo viene ignorata seKeepSourceFormatting viene utilizzata la modalità. Il valore predefinito è`VERO` .

```csharp
public bool IgnoreTextBoxes { get; set; }
```

## Esempi

Mostra come gestire la formattazione della casella di testo durante l'aggiunta di un documento.

```csharp
// Crea un documento in cui verranno inseriti nodi provenienti da un altro documento.
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

builder.Writeln("Hello world!");

// Creiamo un altro documento con una casella di testo, che importeremo nel primo documento.
Document srcDoc = new Document();
builder = new DocumentBuilder(srcDoc);

Shape textBox = builder.InsertShape(ShapeType.TextBox, 300, 100);
builder.MoveTo(textBox.FirstParagraph);
builder.ParagraphFormat.Style.Font.Name = "Courier New";
builder.ParagraphFormat.Style.Font.Size = 24;
builder.Write("Textbox contents");

// Imposta un flag per specificare se cancellare o preservare la formattazione della casella di testo
// durante l'importazione in altri documenti.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreTextBoxes = ignoreTextBoxes;

// Importa la casella di testo dal documento di origine al documento di destinazione,
// e quindi verificare se abbiamo mantenuto lo stile del contenuto del testo.
NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);
Shape importedTextBox = (Shape)importer.ImportNode(textBox, true);
dstDoc.FirstSection.Body.Paragraphs[1].AppendChild(importedTextBox);

if (ignoreTextBoxes)
{
    Assert.AreEqual(12.0d, importedTextBox.FirstParagraph.Runs[0].Font.Size);
    Assert.AreEqual("Times New Roman", importedTextBox.FirstParagraph.Runs[0].Font.Name);
}
else
{
    Assert.AreEqual(24.0d, importedTextBox.FirstParagraph.Runs[0].Font.Size);
    Assert.AreEqual("Courier New", importedTextBox.FirstParagraph.Runs[0].Font.Name);
}

dstDoc.Save(ArtifactsDir + "DocumentBuilder.IgnoreTextBoxes.docx");
```

### Guarda anche

* class [ImportFormatOptions](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
