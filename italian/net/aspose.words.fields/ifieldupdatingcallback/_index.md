---
title: IFieldUpdatingCallback Interface
linktitle: IFieldUpdatingCallback
articleTitle: IFieldUpdatingCallback
second_title: Aspose.Words per .NET
description: Personalizza gli aggiornamenti dei campi in Aspose.Words con l'interfaccia IFieldUpdatingCallback. Migliora le funzionalità con i tuoi metodi per l'elaborazione personalizzata dei documenti.
type: docs
weight: 3130
url: /it/net/aspose.words.fields/ifieldupdatingcallback/
---
## IFieldUpdatingCallback interface

Implementa questa interfaccia se vuoi che vengano chiamati i tuoi metodi personalizzati durante un aggiornamento di campo.

```csharp
public interface IFieldUpdatingCallback
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| [FieldUpdated](../../aspose.words.fields/ifieldupdatingcallback/fieldupdated/)(*[Field](../field/)*) | Un metodo definito dall'utente che viene chiamato subito dopo l'aggiornamento di un campo. |
| [FieldUpdating](../../aspose.words.fields/ifieldupdatingcallback/fieldupdating/)(*[Field](../field/)*) | Un metodo definito dall'utente che viene chiamato subito prima che un campo venga aggiornato. |

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

* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
