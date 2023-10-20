---
title: TxtSaveOptions.PreserveTableLayout
linktitle: PreserveTableLayout
articleTitle: PreserveTableLayout
second_title: Aspose.Words per .NET
description: TxtSaveOptions PreserveTableLayout proprietà. Specifica se il programma deve tentare di preservare il layout delle tabelle durante il salvataggio in formato testo normale. Il valore predefinito èfalso  in C#.
type: docs
weight: 50
url: /it/net/aspose.words.saving/txtsaveoptions/preservetablelayout/
---
## TxtSaveOptions.PreserveTableLayout property

Specifica se il programma deve tentare di preservare il layout delle tabelle durante il salvataggio in formato testo normale. Il valore predefinito è`falso` .

```csharp
public bool PreserveTableLayout { get; set; }
```

## Esempi

Mostra come preservare il layout delle tabelle durante la conversione in testo normale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1");
builder.InsertCell();
builder.Write("Row 1, cell 2");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, cell 1");
builder.InsertCell();
builder.Write("Row 2, cell 2");
builder.EndTable();

// Crea un oggetto "TxtSaveOptions", che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui salviamo il documento in testo normale.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Imposta la proprietà "PreserveTableLayout" su "true" per applicare il riempimento degli spazi bianchi al contenuto
// del documento di testo in chiaro di output per preservare quanto più possibile il layout della tabella.
// Imposta la proprietà "PreserveTableLayout" su "false" per salvare il contenuto di tutte le tabelle
// come un corpo di testo continuo, con solo una nuova riga per ogni riga.
txtSaveOptions.PreserveTableLayout = preserveTableLayout;

doc.Save(ArtifactsDir + "TxtSaveOptions.PreserveTableLayout.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.PreserveTableLayout.txt");

if (preserveTableLayout)
    Assert.AreEqual("Row 1, cell 1                                            Row 1, cell 2\r\n" +
                    "Row 2, cell 1                                            Row 2, cell 2\r\n\r\n", docText);
else
    Assert.AreEqual("Row 1, cell 1\r" +
                    "Row 1, cell 2\r" +
                    "Row 2, cell 1\r" +
                    "Row 2, cell 2\r\r\n", docText);
```

### Guarda anche

* class [TxtSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
