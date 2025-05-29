---
title: FieldUpdatingProgressArgs.TotalFieldsCount
linktitle: TotalFieldsCount
articleTitle: TotalFieldsCount
second_title: Aspose.Words per .NET
description: Scopri la proprietà TotalFieldsCount in FieldUpdatingProgressArgs per monitorare e gestire in modo efficiente gli aggiornamenti dei campi e ottenere prestazioni migliori.
type: docs
weight: 10
url: /it/net/aspose.words.fields/fieldupdatingprogressargs/totalfieldscount/
---
## FieldUpdatingProgressArgs.TotalFieldsCount property

Ottiene il conteggio totale dei campi da aggiornare.

```csharp
public int TotalFieldsCount { get; }
```

## Osservazioni

Il valore non è costante e potrebbe essere aumentato durante il processo di aggiornamento.

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

* class [FieldUpdatingProgressArgs](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
