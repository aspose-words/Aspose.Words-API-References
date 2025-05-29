---
title: FieldOptions.DefaultDocumentAuthor
linktitle: DefaultDocumentAuthor
articleTitle: DefaultDocumentAuthor
second_title: Aspose.Words per .NET
description: Gestisci la proprietà DefaultDocumentAuthor per impostare o aggiornare facilmente i nomi degli autori dei documenti, migliorando così l'efficienza dell'organizzazione e della gestione dei documenti.
type: docs
weight: 70
url: /it/net/aspose.words.fields/fieldoptions/defaultdocumentauthor/
---
## FieldOptions.DefaultDocumentAuthor property

Ottiene o imposta il nome predefinito dell'autore del documento. Se il nome dell'autore è già specificato nelle proprietà predefinite del documento, questa opzione non viene considerata.

```csharp
public string DefaultDocumentAuthor { get; set; }
```

## Esempi

Mostra come utilizzare un campo AUTORE per visualizzare il nome del creatore di un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// I campi AUTHOR ricavano i risultati dalla proprietà del documento integrata denominata "Author".
// Se creiamo e salviamo un documento in Microsoft Word,
// conterrà il nostro nome utente in quella proprietà.
// Tuttavia, se creiamo un documento a livello di programmazione utilizzando Aspose.Words,
// la proprietà "Autore", per impostazione predefinita, sarà una stringa vuota.
Assert.AreEqual(string.Empty, doc.BuiltInDocumentProperties.Author);

// Imposta un nome autore di backup per i campi AUTORE da utilizzare
// se la proprietà "Author" contiene una stringa vuota.
doc.FieldOptions.DefaultDocumentAuthor = "Joe Bloggs";

builder.Write("This document was created by ");
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("Joe Bloggs", field.Result);

// Aggiornamento di un campo AUTORE che contiene un valore
// applicherà quel valore alla proprietà incorporata "Author".
Assert.AreEqual("Joe Bloggs", doc.BuiltInDocumentProperties.Author);

// Modificando questa proprietà e quindi aggiornando il campo AUTORE, questo valore verrà applicato al campo.
doc.BuiltInDocumentProperties.Author = "John Doe";
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

// Se aggiorniamo un campo AUTORE dopo aver modificato la sua proprietà "Nome",
// quindi il campo visualizzerà il nuovo nome e applicherà il nuovo nome alla proprietà incorporata.
field.AuthorName = "Jane Doe";
field.Update();

Assert.AreEqual(" AUTHOR  \"Jane Doe\"", field.GetFieldCode());
Assert.AreEqual("Jane Doe", field.Result);

// I campi AUTHOR non influiscono sulla proprietà DefaultDocumentAuthor.
Assert.AreEqual("Jane Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Joe Bloggs", doc.FieldOptions.DefaultDocumentAuthor);

doc.Save(ArtifactsDir + "Field.AUTHOR.docx");
```

### Guarda anche

* class [FieldOptions](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
