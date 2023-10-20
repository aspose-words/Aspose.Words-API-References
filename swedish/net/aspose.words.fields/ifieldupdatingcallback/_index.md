---
title: IFieldUpdatingCallback Interface
linktitle: IFieldUpdatingCallback
articleTitle: IFieldUpdatingCallback
second_title: Aspose.Words för .NET
description: Aspose.Words.Fields.IFieldUpdatingCallback gränssnitt. Implementera detta gränssnitt om du vill att dina egna anpassade metoder ska anropas under en fältuppdatering i C#.
type: docs
weight: 2720
url: /sv/net/aspose.words.fields/ifieldupdatingcallback/
---
## IFieldUpdatingCallback interface

Implementera detta gränssnitt om du vill att dina egna anpassade metoder ska anropas under en fältuppdatering.

```csharp
public interface IFieldUpdatingCallback
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| [FieldUpdated](../../aspose.words.fields/ifieldupdatingcallback/fieldupdated/)(*[Field](../field/)*) | En användardefinierad metod som anropas precis efter att ett fält har uppdaterats. |
| [FieldUpdating](../../aspose.words.fields/ifieldupdatingcallback/fieldupdating/)(*[Field](../field/)*) | En användardefinierad metod som anropas precis innan ett fält uppdateras. |

## Exempel

Visar hur man använder återuppringningsmetoder under en fältuppdatering.

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
/// Implementera detta gränssnitt om du vill ha dina egna anpassade metoder anropade under en fältuppdatering.
/// </summary>
public class FieldUpdatingCallback : IFieldUpdatingCallback, IFieldUpdatingProgressCallback
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

    void IFieldUpdatingProgressCallback.Notify(FieldUpdatingProgressArgs args)
    {
        Console.WriteLine($"{args.UpdateCompleted}/{args.TotalFieldsCount}");
        Console.WriteLine($"{args.UpdatedFieldsCount}");
    }

    public IList<string> FieldUpdatedCalls { get; }
}
```

### Se även

* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
