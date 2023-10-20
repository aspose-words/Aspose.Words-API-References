---
title: LoadOptions.UpdateDirtyFields
linktitle: UpdateDirtyFields
articleTitle: UpdateDirtyFields
second_title: Aspose.Words per .NET
description: LoadOptions UpdateDirtyFields proprietà. Specifica se aggiornare i campi con ilsporco attributo in C#.
type: docs
weight: 160
url: /it/net/aspose.words.loading/loadoptions/updatedirtyfields/
---
## LoadOptions.UpdateDirtyFields property

Specifica se aggiornare i campi con il`sporco` attributo.

```csharp
public bool UpdateDirtyFields { get; set; }
```

## Esempi

Mostra come utilizzare la proprietà speciale per aggiornare il risultato del campo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Assegna il valore della proprietà "Autore" incorporata al documento, quindi visualizzalo con un campo.
doc.BuiltInDocumentProperties.Author = "John Doe";
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);

Assert.False(field.IsDirty);
Assert.AreEqual("John Doe", field.Result);

// Aggiorna la proprietà. Il campo visualizza ancora il vecchio valore.
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

    // L'aggiornamento di campi sporchi come questo imposta automaticamente il loro flag "IsDirty" su false.
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

* class [LoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
