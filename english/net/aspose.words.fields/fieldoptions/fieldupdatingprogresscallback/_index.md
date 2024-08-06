---
title: FieldOptions.FieldUpdatingProgressCallback
linktitle: FieldUpdatingProgressCallback
articleTitle: FieldUpdatingProgressCallback
second_title: Aspose.Words for .NET
description: FieldOptions FieldUpdatingProgressCallback property. Gets or sets IFieldUpdatingProgressCallback implementation in C#.
type: docs
weight: 130
url: /net/aspose.words.fields/fieldoptions/fieldupdatingprogresscallback/
---
## FieldOptions.FieldUpdatingProgressCallback property

Gets or sets [`IFieldUpdatingProgressCallback`](../../ifieldupdatingprogresscallback/) implementation.

```csharp
public IFieldUpdatingProgressCallback FieldUpdatingProgressCallback { get; set; }
```

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

* interface [IFieldUpdatingProgressCallback](../../ifieldupdatingprogresscallback/)
* class [FieldOptions](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
