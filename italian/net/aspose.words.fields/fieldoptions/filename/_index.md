---
title: FieldOptions.FileName
linktitle: FileName
articleTitle: FileName
second_title: Aspose.Words per .NET
description: FieldOptions FileName proprietà. Ottiene o imposta il nome del file del documento in C#.
type: docs
weight: 140
url: /it/net/aspose.words.fields/fieldoptions/filename/
---
## FieldOptions.FileName property

Ottiene o imposta il nome del file del documento.

```csharp
public string FileName { get; set; }
```

## Osservazioni

Questa proprietà è utilizzata da[`FieldFileName`](../../fieldfilename/) campo con priorità più alta di[`OriginalFileName`](../../../aspose.words/document/originalfilename/) proprietà.

## Esempi

Mostra come utilizzare FieldOptions per sovrascrivere il valore predefinito per il campo FILENAME.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
builder.Writeln();

// Questo campo FILENAME visualizzerà il nome del file di sistema locale del documento che abbiamo caricato.
FieldFileName field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.Update();

Assert.AreEqual(" FILENAME ", field.GetFieldCode());
Assert.AreEqual("Document.docx", field.Result);

builder.Writeln();

// Per impostazione predefinita, il campo FILENAME mostra il nome del file, ma non il percorso completo del file system locale.
// Possiamo impostare un flag per mostrare il percorso completo del file.
field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.IncludeFullPath = true;
field.Update();

Assert.AreEqual(MyDir + "Document.docx", field.Result);

// Possiamo anche impostare un valore per questa proprietà
// sovrascrive il valore visualizzato nel campo FILENAME.
doc.FieldOptions.FileName = "FieldOptions.FILENAME.docx";
field.Update();

Assert.AreEqual(" FILENAME  \\p", field.GetFieldCode());
Assert.AreEqual("FieldOptions.FILENAME.docx", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + doc.FieldOptions.FileName);
```

### Guarda anche

* class [FieldOptions](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
