---
title: FieldOptions.FieldUpdatingCallback
linktitle: FieldUpdatingCallback
articleTitle: FieldUpdatingCallback
second_title: Aspose.Words för .NET
description: Upptäck FieldOptions FieldUpdatingCallback-egenskapen för att enkelt hantera iFieldUpdatingCallback-implementeringar och förbättra effektiviteten i din datahantering.
type: docs
weight: 120
url: /sv/net/aspose.words.fields/fieldoptions/fieldupdatingcallback/
---
## FieldOptions.FieldUpdatingCallback property

Hämtar eller sätter[`IFieldUpdatingCallback`](../../ifieldupdatingcallback/) implementering

```csharp
public IFieldUpdatingCallback FieldUpdatingCallback { get; set; }
```

## Exempel

Visar hur man använder återanropsmetoder under en fältuppdatering.

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
/// Implementera detta gränssnitt om du vill att dina egna anpassade metoder anropas under en fältuppdatering.
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

* interface [IFieldUpdatingCallback](../../ifieldupdatingcallback/)
* class [FieldOptions](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
