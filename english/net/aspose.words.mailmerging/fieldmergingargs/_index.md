---
title: FieldMergingArgs Class
linktitle: FieldMergingArgs
articleTitle: FieldMergingArgs
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.MailMerging.FieldMergingArgs class for seamless data handling in MergeField events, enhancing your document processing experience.
type: docs
weight: 4460
url: /net/aspose.words.mailmerging/fieldmergingargs/
---
## FieldMergingArgs class

Provides data for the **MergeField** event.

To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/net/mail-merge-and-reporting/) documentation article.

```csharp
public class FieldMergingArgs : FieldMergingArgsBase
```

## Properties

| Name | Description |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document/) { get; } | Returns the [`Document`](../fieldmergingargsbase/document/) object for which the mail merge is performed. |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/) { get; } | Gets the name of the merge field as specified in the document. |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field/) { get; } | Gets the object that represents the current merge field. |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname/) { get; } | Gets the name of the merge field in the data source. |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/) { get; set; } | Gets or sets the value of the field from the data source. |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex/) { get; } | Gets the zero based index of the record that is being merged. |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename/) { get; } | Gets the name of the data table for the current merge operation or empty string if the name is not available. |
| [Text](../../aspose.words.mailmerging/fieldmergingargs/text/) { get; set; } | Gets or sets the text that will be inserted into the document for the current merge field. |

## Remarks

The **MergeField** event occurs during mail merge when a simple mail merge field is encountered in the document. You can respond to this event to return text for the mail merge engine to insert into the document.

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

* class [FieldMergingArgsBase](../fieldmergingargsbase/)
* namespace [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../)
