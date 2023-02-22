---
title: IFieldUpdatingCallback.FieldUpdating
second_title: Aspose.Words för .NET API Referens
description: IFieldUpdatingCallback metod. En användardefinierad metod som anropas precis innan ett fält uppdateras.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/ifieldupdatingcallback/fieldupdating/
---
## IFieldUpdatingCallback.FieldUpdating method

En användardefinierad metod som anropas precis innan ett fält uppdateras.

```csharp
public void FieldUpdating(Field field)
```

### Exempel

Visar hur man använder återuppringningsmetoder under en fältuppdatering.

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
/// Implementera detta gränssnitt om du vill ha dina egna anpassade metoder anropade under en fältuppdatering.
/// </summary>
public class FieldUpdatingCallback : IFieldUpdatingCallback
{
    public FieldUpdatingCallback()
    {
        FieldUpdatedCalls = new List<string>();
    }

    /// <summary>
    /// En användardefinierad metod som anropas precis innan ett fält uppdateras.
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
    /// En användardefinierad metod som anropas precis efter att ett fält har uppdaterats.
    /// </summary>
    void IFieldUpdatingCallback.FieldUpdated(Field field)
    {
        FieldUpdatedCalls.Add(field.Result);
    }

    public IList<string> FieldUpdatedCalls { get; }
}
```

### Se även

* class [Field](../../field/)
* interface [IFieldUpdatingCallback](../)
* namnutrymme [Aspose.Words.Fields](../../ifieldupdatingcallback/)
* hopsättning [Aspose.Words](../../../)


