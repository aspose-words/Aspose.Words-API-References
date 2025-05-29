---
title: TxtSaveOptions.PreserveTableLayout
linktitle: PreserveTableLayout
articleTitle: PreserveTableLayout
second_title: Aspose.Words per .NET
description: Scopri la funzione PreserveTableLayout di TxtSaveOptions, che garantisce che le tue tabelle mantengano il loro layout quando vengono salvate come testo normale. Migliora la leggibilità del tuo documento!
type: docs
weight: 50
url: /it/net/aspose.words.saving/txtsaveoptions/preservetablelayout/
---
## TxtSaveOptions.PreserveTableLayout property

Specifica se il programma deve tentare di preservare il layout delle tabelle durante il salvataggio nel formato di testo normale. Il valore predefinito è`falso` .

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

// Creiamo un oggetto "TxtSaveOptions", che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui salviamo il documento in testo normale.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Imposta la proprietà "PreserveTableLayout" su "true" per applicare la spaziatura al contenuto
// del documento di testo normale di output per preservare il più possibile il layout della tabella.
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
