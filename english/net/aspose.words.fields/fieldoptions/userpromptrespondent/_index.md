---
title: FieldOptions.UserPromptRespondent
linktitle: UserPromptRespondent
second_title: Aspose.Words for .NET API Reference
description: FieldOptions property. Gets or sets the respondent to user prompts during field update in C#.
type: docs
weight: 210
url: /net/aspose.words.fields/fieldoptions/userpromptrespondent/
---
## FieldOptions.UserPromptRespondent property

Gets or sets the respondent to user prompts during field update.

```csharp
public IFieldUserPromptRespondent UserPromptRespondent { get; set; }
```

## Remarks

If the value of this property is set to `null`, the fields that require user response on prompting (such as [`FieldAsk`](../../fieldask/) or [`FieldFillIn`](../../fieldfillin/)) are not updated.

The default value is `null`.

## Examples

Shows how to create an ASK field, and set its properties.

```csharp
[Test]
public void FieldAsk()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Place a field where the response to our ASK field will be placed.
    FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    fieldRef.BookmarkName = "MyAskField";
    builder.Writeln();

    Assert.AreEqual(" REF  MyAskField", fieldRef.GetFieldCode());

    // Insert the ASK field and edit its properties to reference our REF field by bookmark name.
    FieldAsk fieldAsk = (FieldAsk)builder.InsertField(FieldType.FieldAsk, true);
    fieldAsk.BookmarkName = "MyAskField";
    fieldAsk.PromptText = "Please provide a response for this ASK field";
    fieldAsk.DefaultResponse = "Response from within the field.";
    fieldAsk.PromptOnceOnMailMerge = true;
    builder.Writeln();

    Assert.AreEqual(
        " ASK  MyAskField \"Please provide a response for this ASK field\" \\d \"Response from within the field.\" \\o",
        fieldAsk.GetFieldCode());

    // ASK fields apply the default response to their respective REF fields during a mail merge.
    DataTable table = new DataTable("My Table");
    table.Columns.Add("Column 1");
    table.Rows.Add("Row 1");
    table.Rows.Add("Row 2");

    FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    fieldMergeField.FieldName = "Column 1";

    // We can modify or override the default response in our ASK fields with a custom prompt responder,
    // which will occur during a mail merge.
    doc.FieldOptions.UserPromptRespondent = new MyPromptRespondent();
    doc.MailMerge.Execute(table);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.ASK.docx");
}

/// <summary>
/// Prepends text to the default response of an ASK field during a mail merge.
/// </summary>
private class MyPromptRespondent : IFieldUserPromptRespondent
{
    public string Respond(string promptText, string defaultResponse)
    {
        return "Response from MyPromptRespondent. " + defaultResponse;
    }
}
```

### See Also

* interface [IFieldUserPromptRespondent](../../ifielduserpromptrespondent/)
* class [FieldOptions](../)
* namespace [Aspose.Words.Fields](../../fieldoptions/)
* assembly [Aspose.Words](../../../)
