---
title: FieldValue
second_title: Aspose.Words for .NET API Reference
description: FieldMergingArgsBase property. Gets or sets the value of the field from the data source in C#.
type: docs
weight: 50
url: /net/aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/
---
## FieldMergingArgsBase.FieldValue property

Gets or sets the value of the field from the data source.

```csharp
public object FieldValue { get; set; }
```

## Remarks

This property contains a value that has just been selected from your data source for this field by the mail merge engine. You can also replace the value by setting the property.

## Examples

Shows how to edit values that MERGEFIELDs receive as a mail merge takes place.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Insert some MERGEFIELDs with format switches that will edit the values they will receive during a mail merge.
    builder.InsertField("MERGEFIELD text_Field1 \\* Caps", null);
    builder.Write(", ");
    builder.InsertField("MERGEFIELD text_Field2 \\* Upper", null);
    builder.Write(", ");
    builder.InsertField("MERGEFIELD numeric_Field1 \\# 0.0", null);

    builder.Document.MailMerge.FieldMergingCallback = new FieldValueMergingCallback();

    builder.Document.MailMerge.Execute(
        new string[] { "text_Field1", "text_Field2", "numeric_Field1" },
        new object[] { "Field 1", "Field 2", 10 });
    string t = doc.GetText().Trim();
    Assert.AreEqual("Merge Value For \"Text_Field1\": Field 1, MERGE VALUE FOR \"TEXT_FIELD2\": FIELD 2, 10000.0", doc.GetText().Trim());
}

/// <summary>
/// Edits the values that MERGEFIELDs receive during a mail merge.
/// The name of a MERGEFIELD must have a prefix for this callback to take effect on its value.
/// </summary>
private class FieldValueMergingCallback : IFieldMergingCallback
{
    /// <summary>
    /// Called when a mail merge merges data into a MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs e)
    {
        if (e.FieldName.StartsWith("text_"))
            e.FieldValue = $"Merge value for \"{e.FieldName}\": {(string)e.FieldValue}";
        else if (e.FieldName.StartsWith("numeric_"))
            e.FieldValue = (int)e.FieldValue * 1000;
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        // Do nothing.
    }
}
```

### See Also

* class [FieldMergingArgsBase](../)
* namespace [Aspose.Words.MailMerging](../../fieldmergingargsbase/)
* assembly [Aspose.Words](../../../)
