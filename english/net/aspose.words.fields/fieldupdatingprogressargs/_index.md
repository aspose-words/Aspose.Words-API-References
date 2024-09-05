---
title: FieldUpdatingProgressArgs Class
linktitle: FieldUpdatingProgressArgs
articleTitle: FieldUpdatingProgressArgs
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.FieldUpdatingProgressArgs class. Provides data for the field updating progress event in C#.
type: docs
weight: 2830
url: /net/aspose.words.fields/fieldupdatingprogressargs/
---
## FieldUpdatingProgressArgs class

Provides data for the field updating progress event.

```csharp
public sealed class FieldUpdatingProgressArgs
```

## Properties

| Name | Description |
| --- | --- |
| [TotalFieldsCount](../../aspose.words.fields/fieldupdatingprogressargs/totalfieldscount/) { get; } | Gets the total fields count to be updated. |
| [UpdateCompleted](../../aspose.words.fields/fieldupdatingprogressargs/updatecompleted/) { get; } | Gets a value indicating whether field updating is completed. |
| [UpdatedFieldsCount](../../aspose.words.fields/fieldupdatingprogressargs/updatedfieldscount/) { get; } | Gets the number of updated fields. |

## Examples

Shows how to use callback methods during a field update.

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
/// Implement this interface if you want to have your own custom methods called during a field update.
/// </summary>
public class FieldUpdatingCallback : IFieldUpdatingCallback, IFieldUpdatingProgressCallback
{
    public FieldUpdatingCallback()
    {
        FieldUpdatedCalls = new List<string>();
    }

    /// <summary>
    /// A user defined method that is called just before a field is updated.
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
    /// A user defined method that is called just after a field is updated.
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

### See Also

* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
