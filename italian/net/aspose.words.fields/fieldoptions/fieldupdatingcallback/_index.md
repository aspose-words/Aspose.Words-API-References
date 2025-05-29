---
title: FieldOptions.FieldUpdatingCallback
linktitle: FieldUpdatingCallback
articleTitle: FieldUpdatingCallback
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldOptions FieldUpdatingCallback per gestire facilmente le implementazioni IFieldUpdatingCallback e migliorare l'efficienza nella gestione dei dati.
type: docs
weight: 120
url: /it/net/aspose.words.fields/fieldoptions/fieldupdatingcallback/
---
## FieldOptions.FieldUpdatingCallback property

Ottiene o imposta[`IFieldUpdatingCallback`](../../ifieldupdatingcallback/) implementazione

```csharp
public IFieldUpdatingCallback FieldUpdatingCallback { get; set; }
```

## Esempi

Mostra come utilizzare i metodi di callback durante l'aggiornamento di un campo.

```csharp
public void FieldUpdatingCallbackTest()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
    builder.InsertField(" TIME ");
    builder.InsertField(" REVNUM ");
    builder.InsertField(" AUTHOR  \"John Doe\" ");
    builder.InsertField(" SUBJECT \"My Subject\" ");
    builder.InsertField(" QUOTE \"Hello world!\" ");

    FieldUpdatingCallback callback = new FieldUpdatingCallback();
    doc.FieldOptions.FieldUpdatingCallback = callback;

    doc.UpdateFields();

    Assert.True(callback.FieldUpdatedCalls.Contains("Updating John Doe"));
}

/// <summary>
/// Implementa questa interfaccia se vuoi che vengano chiamati metodi personalizzati durante un aggiornamento di campo.
/// </summary>
public class FieldUpdatingCallback : IFieldUpdatingCallback, IFieldUpdatingProgressCallback
{
    public FieldUpdatingCallback()
    {
        FieldUpdatedCalls = new List<string>();
    }

    /// <summary>
    /// Metodo definito dall'utente che viene chiamato subito prima dell'aggiornamento di un campo.
    /// </summary>
    void IFieldUpdatingCallback.FieldUpdating(Field field)
    {
        if (field.Type == FieldType.FieldAuthor)
        {
            FieldAuthor fieldAuthor = (FieldAuthor) field;
            fieldAuthor.AuthorName = "Updating John Doe";
        }
    }

    /// <summary>
    /// Metodo definito dall'utente che viene chiamato subito dopo l'aggiornamento di un campo.
    /// </summary>
    void IFieldUpdatingCallback.FieldUpdated(Field field)
    {
        FieldUpdatedCalls.Add(field.Result);
    }

    void IFieldUpdatingProgressCallback.Notify(FieldUpdatingProgressArgs args)
    {
        Console.WriteLine($"{args.UpdateCompleted}/{args.TotalFieldsCount}");
        Console.WriteLine($"{args.UpdatedFieldsCount}");
    }

    public IList<string> FieldUpdatedCalls { get; }
}
```

### Guarda anche

* interface [IFieldUpdatingCallback](../../ifieldupdatingcallback/)
* class [FieldOptions](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
