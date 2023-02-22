---
title: IFieldUpdatingCallback.FieldUpdated
second_title: Aspose.Words für .NET-API-Referenz
description: IFieldUpdatingCallback methode. Eine benutzerdefinierte Methode die unmittelbar nach der Aktualisierung eines Felds aufgerufen wird.
type: docs
weight: 10
url: /de/net/aspose.words.fields/ifieldupdatingcallback/fieldupdated/
---
## IFieldUpdatingCallback.FieldUpdated method

Eine benutzerdefinierte Methode, die unmittelbar nach der Aktualisierung eines Felds aufgerufen wird.

```csharp
public void FieldUpdated(Field field)
```

### Beispiele

Zeigt, wie Callback-Methoden während einer Feldaktualisierung verwendet werden.

```csharp
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
/// Implementieren Sie diese Schnittstelle, wenn Sie möchten, dass Ihre eigenen benutzerdefinierten Methoden während einer Feldaktualisierung aufgerufen werden.
/// </summary>
public class FieldUpdatingCallback : IFieldUpdatingCallback
{
    public FieldUpdatingCallback()
    {
        FieldUpdatedCalls = new List<string>();
    }

    /// <summary>
    /// Eine benutzerdefinierte Methode, die aufgerufen wird, kurz bevor ein Feld aktualisiert wird.
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

    public IList<string> FieldUpdatedCalls { get; }
}
```

### Siehe auch

* class [Field](../../field/)
* interface [IFieldUpdatingCallback](../)
* namensraum [Aspose.Words.Fields](../../ifieldupdatingcallback/)
* Montage [Aspose.Words](../../../)


