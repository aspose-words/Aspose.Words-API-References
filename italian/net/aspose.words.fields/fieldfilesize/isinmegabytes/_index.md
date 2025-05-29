---
title: FieldFileSize.IsInMegabytes
linktitle: IsInMegabytes
articleTitle: IsInMegabytes
second_title: Aspose.Words per .NET
description: Controlla la visualizzazione delle dimensioni dei file con la proprietà IsInMegabytes di FieldFileSize. Passa facilmente da byte a megabyte per una maggiore chiarezza e un'esperienza utente migliore.
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldfilesize/isinmegabytes/
---
## FieldFileSize.IsInMegabytes property

Ottiene o imposta se visualizzare la dimensione del file in megabyte.

```csharp
public bool IsInMegabytes { get; set; }
```

## Esempi

Mostra come visualizzare la dimensione del file di un documento con un campo FILESIZE.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(18105, doc.BuiltInDocumentProperties.Bytes);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertParagraph();

// Di seguito sono riportate tre diverse unità di misura
// con cui i campi FILESIZE possono visualizzare la dimensione del file del documento.
// 1 - Byte:
FieldFileSize field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.Update();

Assert.AreEqual(" FILESIZE ", field.GetFieldCode());
Assert.AreEqual("18105", field.Result);

// 2 - Kilobyte:
builder.InsertParagraph();
field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.IsInKilobytes = true;
field.Update();

Assert.AreEqual(" FILESIZE  \\k", field.GetFieldCode());
Assert.AreEqual("18", field.Result);

// 3 - Megabyte:
builder.InsertParagraph();
field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.IsInMegabytes = true;
field.Update();

Assert.AreEqual(" FILESIZE  \\m", field.GetFieldCode());
Assert.AreEqual("0", field.Result);

// Per aggiornare i valori di questi campi durante la modifica in Microsoft Word,
// dobbiamo prima salvare le modifiche e poi aggiornare manualmente questi campi.
doc.Save(ArtifactsDir + "Field.FILESIZE.docx");
```

### Guarda anche

* class [FieldFileSize](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
