---
title: FieldAuthor.AuthorName
linktitle: AuthorName
articleTitle: AuthorName
second_title: Aspose.Words per .NET
description: Gestisci gli autori dei documenti senza sforzo con FieldAuthor AuthorName. Ottieni o imposta facilmente i nomi degli autori per migliorare l'affidabilità e l'organizzazione dei tuoi contenuti.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldauthor/authorname/
---
## FieldAuthor.AuthorName property

Ottiene o imposta il nome dell'autore del documento.

```csharp
public string AuthorName { get; set; }
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

* class [FieldAuthor](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
