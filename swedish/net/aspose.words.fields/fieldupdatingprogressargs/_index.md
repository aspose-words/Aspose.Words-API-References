---
title: FieldUpdatingProgressArgs Class
linktitle: FieldUpdatingProgressArgs
articleTitle: FieldUpdatingProgressArgs
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.FieldUpdatingProgressArgs, som förbättrar din dokumentautomation genom att ge realtidsuppdateringar om fältförloppet.
type: docs
weight: 2980
url: /sv/net/aspose.words.fields/fieldupdatingprogressargs/
---
## FieldUpdatingProgressArgs class

Tillhandahåller data för händelsen för fältuppdateringsförloppet.

```csharp
public sealed class FieldUpdatingProgressArgs
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [TotalFieldsCount](../../aspose.words.fields/fieldupdatingprogressargs/totalfieldscount/) { get; } | Hämtar det totala antalet fält som ska uppdateras. |
| [UpdateCompleted](../../aspose.words.fields/fieldupdatingprogressargs/updatecompleted/) { get; } | Hämtar ett värde som anger om fältuppdateringen är slutförd. |
| [UpdatedFieldsCount](../../aspose.words.fields/fieldupdatingprogressargs/updatedfieldscount/) { get; } | Hämtar antalet uppdaterade fält. |

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

* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
