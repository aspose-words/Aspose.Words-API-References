---
title: FieldSet.BookmarkName
linktitle: BookmarkName
articleTitle: BookmarkName
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldSet BookmarkName per gestire e personalizzare facilmente i tuoi segnalibri. Migliora la navigazione della tua applicazione con questa funzionalità fondamentale!
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldset/bookmarkname/
---
## FieldSet.BookmarkName property

Ottiene o imposta il nome del segnalibro.

```csharp
public string BookmarkName { get; set; }
```

## Esempi

Mostra come creare testo con segnalibro con un campo SET e poi visualizzarlo nel documento utilizzando un campo REF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Assegna un nome al testo aggiunto ai preferiti con un campo SET.
// Questo campo si riferisce al "segnalibro", non a una struttura di segnalibro che appare all'interno del testo, ma a una variabile denominata.
FieldSet fieldSet = (FieldSet)builder.InsertField(FieldType.FieldSet, false);
fieldSet.BookmarkName = "MyBookmark";
fieldSet.BookmarkText = "Hello world!";
fieldSet.Update();

Assert.AreEqual(" SET  MyBookmark \"Hello world!\"", fieldSet.GetFieldCode());

// Fare riferimento al segnalibro tramite il nome in un campo REF e visualizzarne il contenuto.
FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
fieldRef.BookmarkName = "MyBookmark";
fieldRef.Update();

Assert.AreEqual(" REF  MyBookmark", fieldRef.GetFieldCode());
Assert.AreEqual("Hello world!", fieldRef.Result);

doc.Save(ArtifactsDir + "Field.SET.REF.docx");
```

### Guarda anche

* class [FieldSet](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
