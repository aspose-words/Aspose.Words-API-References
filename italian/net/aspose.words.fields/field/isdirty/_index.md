---
title: Field.IsDirty
linktitle: IsDirty
articleTitle: IsDirty
second_title: Aspose.Words per .NET
description: Gestisci la proprietà IsDirty per garantire che i dati dei tuoi campi siano sempre accurati e aggiornati, migliorando l'integrità e le prestazioni dei documenti.
type: docs
weight: 40
url: /it/net/aspose.words.fields/field/isdirty/
---
## Field.IsDirty property

Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento.

```csharp
public bool IsDirty { get; set; }
```

## Esempi

Mostra come utilizzare una proprietà speciale per aggiornare il risultato del campo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Assegna il valore alla proprietà "Autore" incorporata nel documento, quindi visualizzala con un campo.
doc.BuiltInDocumentProperties.Author = "John Doe";
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);

Assert.False(field.IsDirty);
Assert.AreEqual("John Doe", field.Result);

// Aggiorna la proprietà. Il campo mostra ancora il vecchio valore.
doc.BuiltInDocumentProperties.Author = "John & Jane Doe";

Assert.AreEqual("John Doe", field.Result);

// Poiché il valore del campo non è aggiornato, possiamo contrassegnarlo come "sporco".
// Questo valore rimarrà obsoleto finché non aggiorneremo manualmente il campo con il metodo Field.Update().
field.IsDirty = true;

using (MemoryStream docStream = new MemoryStream())
{
    // Se salviamo senza chiamare un metodo di aggiornamento,
    // il campo continuerà a visualizzare il valore scaduto nel documento di output.
    doc.Save(docStream, SaveFormat.Docx);

    // L'oggetto LoadOptions ha un'opzione per aggiornare tutti i campi
    // contrassegnato come "sporco" durante il caricamento del documento.
    LoadOptions options = new LoadOptions();
    options.UpdateDirtyFields = updateDirtyFields;
    doc = new Document(docStream, options);

    Assert.AreEqual("John & Jane Doe", doc.BuiltInDocumentProperties.Author);

    field = (FieldAuthor)doc.Range.Fields[0];

    // L'aggiornamento dei campi dirty in questo modo imposta automaticamente il loro flag "IsDirty" su false.
    if (updateDirtyFields)
    {
        Assert.AreEqual("John & Jane Doe", field.Result);
        Assert.False(field.IsDirty);
    }
    else
    {
        Assert.AreEqual("John Doe", field.Result);
        Assert.True(field.IsDirty);
    }
}
```

### Guarda anche

* class [Field](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
