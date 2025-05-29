---
title: FieldFileName.IncludeFullPath
linktitle: IncludeFullPath
articleTitle: IncludeFullPath
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldFileName IncludeFullPath e gestisci facilmente i percorsi dei file con impostazioni personalizzabili per una migliore gestione e organizzazione dei file.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldfilename/includefullpath/
---
## FieldFileName.IncludeFullPath property

Ottiene o imposta se includere il nome completo del percorso del file.

```csharp
public bool IncludeFullPath { get; set; }
```

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
// Possiamo impostare un flag per far sì che venga visualizzato il percorso completo del file.
field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.IncludeFullPath = true;
field.Update();

Assert.AreEqual(MyDir + "Document.docx", field.Result);

// Possiamo anche impostare un valore per questa proprietà su
// sovrascrive il valore visualizzato nel campo FILENAME.
doc.FieldOptions.FileName = "FieldOptions.FILENAME.docx";
field.Update();

Assert.AreEqual(" FILENAME  \\p", field.GetFieldCode());
Assert.AreEqual("FieldOptions.FILENAME.docx", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + doc.FieldOptions.FileName);
```

### Guarda anche

* class [FieldFileName](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
