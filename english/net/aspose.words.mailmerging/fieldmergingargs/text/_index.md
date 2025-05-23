---
title: FieldMergingArgs.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: Manage your document's merge fields effortlessly with FieldMergingArgs. Easily set or retrieve text for seamless document integration.
type: docs
weight: 10
url: /net/aspose.words.mailmerging/fieldmergingargs/text/
---
## FieldMergingArgs.Text property

Gets or sets the text that will be inserted into the document for the current merge field.

```csharp
public string Text { get; set; }
```

## Remarks

When your event handler is called, this property is set to `null`.

If you leave Text as `null`, the mail merge engine will insert [`FieldValue`](../../fieldmergingargsbase/fieldvalue/) in place of the merge field.

If you set Text to any string (including empty), the string will be inserted into the document in place of the merge field.

## Examples

Shows how to execute a mail merge with a custom callback that handles merge data in the form of HTML documents.

```csharp
public void MergeHtml()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(@"MERGEFIELD  html_Title  \b Content");
    builder.InsertField(@"MERGEFIELD  html_Body  \b Content");

    object[] mergeData =
    {
        "<html>" +
            "<h1>" +
                "<span style=\"color: #0000ff; font-family: Arial;\">Hello World!</span>" +
            "</h1>" +
        "</html>", 

        "<html>" +
            "<blockquote>" +
                "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>" +
            "</blockquote>" +
        "</html>"
    };

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldInsertHtml();
    doc.MailMerge.Execute(new[] { "html_Title", "html_Body" }, mergeData);

    doc.Save(ArtifactsDir + "MailMergeEvent.MergeHtml.docx");
}

/// <summary>
/// If the mail merge encounters a MERGEFIELD whose name starts with the "html_" prefix,
/// this callback parses its merge data as HTML content and adds the result to the document location of the MERGEFIELD.
/// </summary>
private class HandleMergeFieldInsertHtml : IFieldMergingCallback
{
    /// <summary>
    /// Called when a mail merge merges data into a MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName.StartsWith("html_") && args.Field.GetFieldCode().Contains("\\b"))
        {
            // Add parsed HTML data to the document's body.
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

            // Since we have already inserted the merged content manually,
            // we will not need to respond to this event by returning content via the "Text" property. 
            args.Text = string.Empty;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Do nothing.
    }
}
```

### See Also

* class [FieldMergingArgs](../)
* namespace [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../../)
