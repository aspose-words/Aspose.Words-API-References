---
title: FieldUpdatingProgressArgs.TotalFieldsCount
second_title: Aspose.Words für .NET-API-Referenz
description: FieldUpdatingProgressArgs eigendom. Ruft die Gesamtzahl der zu aktualisierenden Felder ab.
type: docs
weight: 10
url: /de/net/aspose.words.fields/fieldupdatingprogressargs/totalfieldscount/
---
## FieldUpdatingProgressArgs.TotalFieldsCount property

Ruft die Gesamtzahl der zu aktualisierenden Felder ab.

```csharp
public int TotalFieldsCount { get; }
```

### Bemerkungen

Der Wert ist nicht konstant und kann während des Aktualisierungsprozesses erhöht werden.

### Beispiele

Zeigt, wie Callback-Methoden während einer Feldaktualisierung verwendet werden.

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
/// Implementieren Sie diese Schnittstelle, wenn Sie möchten, dass während einer Feldaktualisierung Ihre eigenen benutzerdefinierten Methoden aufgerufen werden.
/// </summary>
public class FieldUpdatingCallback : IFieldUpdatingCallback, IFieldUpdatingProgressCallback
{
    public FieldUpdatingCallback()
    {
        FieldUpdatedCalls = new List<string>();
    }

    /// <summary>
    /// Eine benutzerdefinierte Methode, die aufgerufen wird, unmittelbar bevor ein Feld aktualisiert wird.
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

* class [FieldUpdatingProgressArgs](../)
* namensraum [Aspose.Words.Fields](../../fieldupdatingprogressargs/)
* Montage [Aspose.Words](../../../)


