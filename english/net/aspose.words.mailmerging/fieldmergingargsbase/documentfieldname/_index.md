---
title: FieldMergingArgsBase.DocumentFieldName
linktitle: DocumentFieldName
articleTitle: DocumentFieldName
second_title: Aspose.Words for .NET
description: Discover the DocumentFieldName property of FieldMergingArgsBase. Easily access and manage merge field names for efficient document processing.
type: docs
weight: 20
url: /net/aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/
---
## FieldMergingArgsBase.DocumentFieldName property

Gets the name of the merge field as specified in the document.

```csharp
public string DocumentFieldName { get; }
```

## Remarks

If you have a mapping from a document field name to a different data source field name, then this is the original field name as specified in the document.

If you specified a field name prefix, for example "Image:MyFieldName" in the document, then `DocumentFieldName` returns field name without the prefix, that is "MyFieldName".

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

* class [FieldMergingArgsBase](../)
* namespace [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../../)
