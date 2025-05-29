---
title: IFieldUpdatingProgressCallback Interface
linktitle: IFieldUpdatingProgressCallback
articleTitle: IFieldUpdatingProgressCallback
second_title: Aspose.Words für .NET
description: Verfolgen Sie den Fortschritt der Feldaktualisierung nahtlos mit der Schnittstelle Aspose.Words.Fields.IFieldUpdatingProgressCallback. Verbessern Sie noch heute Ihr Dokumentenmanagement!
type: docs
weight: 3140
url: /de/net/aspose.words.fields/ifieldupdatingprogresscallback/
---
## IFieldUpdatingProgressCallback interface

Implementieren Sie diese Schnittstelle, wenn Sie den Fortschritt der Feldaktualisierung verfolgen möchten.

```csharp
public interface IFieldUpdatingProgressCallback
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Notify](../../aspose.words.fields/ifieldupdatingprogresscallback/notify/)(*[FieldUpdatingProgressArgs](../fieldupdatingprogressargs/)*) | Eine benutzerdefinierte Methode, die aufgerufen wird, wenn sich der Aktualisierungsfortschritt ändert. |

## Beispiele

Zeigt, wie Rückrufmethoden während einer Feldaktualisierung verwendet werden.

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
/// Implementieren Sie diese Schnittstelle, wenn Sie während einer Feldaktualisierung Ihre eigenen benutzerdefinierten Methoden aufrufen möchten.
/// </summary>
public class FieldUpdatingCallback : IFieldUpdatingCallback, IFieldUpdatingProgressCallback
{
    public FieldUpdatingCallback()
    {
        FieldUpdatedCalls = new List<string>();
    }

    /// <summary>
    /// Eine benutzerdefinierte Methode, die unmittelbar vor der Aktualisierung eines Felds aufgerufen wird.
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
    /// Eine benutzerdefinierte Methode, die unmittelbar nach der Aktualisierung eines Felds aufgerufen wird.
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

### Siehe auch

* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
