---
title: IFieldUserPromptRespondent Interface
linktitle: IFieldUserPromptRespondent
articleTitle: IFieldUserPromptRespondent
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Fields.IFieldUserPromptRespondent interface, designed to enhance user interaction and streamline field updates seamlessly.
type: docs
weight: 3140
url: /net/aspose.words.fields/ifielduserpromptrespondent/
---
## IFieldUserPromptRespondent interface

Represents the respondent to user prompts during field update.

```csharp
public interface IFieldUserPromptRespondent
```

## Methods

| Name | Description |
| --- | --- |
| [Respond](../../aspose.words.fields/ifielduserpromptrespondent/respond/)(*string, string*) | When implemented, returns a response from the user on prompting. Your implementation should return `null` to indicate that the user has not responded to the prompt (i.e. the user has pressed the Cancel button in the prompt window). |

## Remarks

The ASK and FILLIN fields are the examples of fields that prompt the user for some response. Implement this interface and assign it to the [`UserPromptRespondent`](../fieldoptions/userpromptrespondent/) property to establish interaction between field update and the user.

## Examples

Shows how to create an ASK field, and set its properties.

```csharp
public void FieldAsk()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Place a field where the response to our ASK field will be placed.
    FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    fieldRef.BookmarkName = "MyAskField";
    builder.Writeln();

    Assert.That(fieldRef.GetFieldCode(), Is.EqualTo(" REF  MyAskField"));

    // Insert the ASK field and edit its properties to reference our REF field by bookmark name.
    FieldAsk fieldAsk = (FieldAsk)builder.InsertField(FieldType.FieldAsk, true);
    fieldAsk.BookmarkName = "MyAskField";
    fieldAsk.PromptText = "Please provide a response for this ASK field";
    fieldAsk.DefaultResponse = "Response from within the field.";
    fieldAsk.PromptOnceOnMailMerge = true;
    builder.Writeln();

    Assert.That(fieldAsk.GetFieldCode(), Is.EqualTo(" ASK  MyAskField \"Please provide a response for this ASK field\" \\d \"Response from within the field.\" \\o"));

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

* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
