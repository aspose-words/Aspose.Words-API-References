---
title: DocumentBuilder.InsertHtml
linktitle: InsertHtml
articleTitle: InsertHtml
second_title: Aspose.Words for .NET
description: Effortlessly enhance your documents with the DocumentBuilder InsertHtml method—seamlessly insert HTML strings for dynamic content integration.
type: docs
weight: 380
url: /net/aspose.words/documentbuilder/inserthtml/
---
## InsertHtml(*string*) {#inserthtml}

Inserts an HTML string into the document.

```csharp
public void InsertHtml(string html)
```

| Parameter | Type | Description |
| --- | --- | --- |
| html | String | An HTML string to insert into the document. |

## Remarks

You can use this method to insert an HTML fragment or whole HTML document.

## Examples

Shows how to use a document builder to insert html content into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

const string html = "<p align='right'>Paragraph right</p>" +
                    "<b>Implicit paragraph left</b>" +
                    "<div align='center'>Div center</div>" +
                    "<h1 align='left'>Heading 1 left.</h1>";

builder.InsertHtml(html);

// Inserting HTML code parses the formatting of each element into equivalent document text formatting.
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.That(paragraphs[0].GetText().Trim(), Is.EqualTo("Paragraph right"));
Assert.That(paragraphs[0].ParagraphFormat.Alignment, Is.EqualTo(ParagraphAlignment.Right));

Assert.That(paragraphs[1].GetText().Trim(), Is.EqualTo("Implicit paragraph left"));
Assert.That(paragraphs[1].ParagraphFormat.Alignment, Is.EqualTo(ParagraphAlignment.Left));
Assert.That(paragraphs[1].Runs[0].Font.Bold, Is.True);

Assert.That(paragraphs[2].GetText().Trim(), Is.EqualTo("Div center"));
Assert.That(paragraphs[2].ParagraphFormat.Alignment, Is.EqualTo(ParagraphAlignment.Center));

Assert.That(paragraphs[3].GetText().Trim(), Is.EqualTo("Heading 1 left."));
Assert.That(paragraphs[3].ParagraphFormat.Style.Name, Is.EqualTo("Heading 1"));

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHtml.docx");
```

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

* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## InsertHtml(*string, bool*) {#inserthtml_2}

Inserts an HTML string into the document.

```csharp
public void InsertHtml(string html, bool useBuilderFormatting)
```

| Parameter | Type | Description |
| --- | --- | --- |
| html | String | An HTML string to insert into the document. |
| useBuilderFormatting | Boolean | A value indicating whether formatting specified in [`DocumentBuilder`](../) is used as base formatting for text imported from HTML. |

## Remarks

You can use this method to insert an HTML fragment or whole HTML document.

When *useBuilderFormatting* is `false`, [`DocumentBuilder`](../) formating is ignored and formatting of inserted text is based on default HTML formatting. As a result, the text looks as it is rendered in browsers.

When *useBuilderFormatting* is `true`, formatting of inserted text is based on [`DocumentBuilder`](../) formatting, and the text looks as if it were inserted with [`Write`](../write/).

## Examples

Shows how to apply a document builder's formatting while inserting HTML content.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Set a text alignment for the builder, insert an HTML paragraph with a specified alignment, and one without.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Distributed;
builder.InsertHtml(
    "<p align='right'>Paragraph 1.</p>" +
    "<p>Paragraph 2.</p>", useBuilderFormatting);

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

// The first paragraph has an alignment specified. When InsertHtml parses the HTML code,
// the paragraph alignment value found in the HTML code always supersedes the document builder's value.
Assert.That(paragraphs[0].GetText().Trim(), Is.EqualTo("Paragraph 1."));
Assert.That(paragraphs[0].ParagraphFormat.Alignment, Is.EqualTo(ParagraphAlignment.Right));

// The second paragraph has no alignment specified. It can have its alignment value filled in
// by the builder's value depending on the flag we passed to the InsertHtml method.
Assert.That(paragraphs[1].GetText().Trim(), Is.EqualTo("Paragraph 2."));
Assert.That(paragraphs[1].ParagraphFormat.Alignment, Is.EqualTo(useBuilderFormatting ? ParagraphAlignment.Distributed : ParagraphAlignment.Left));

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHtmlWithFormatting.docx");
```

### See Also

* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## InsertHtml(*string, [HtmlInsertOptions](../../htmlinsertoptions/)*) {#inserthtml_1}

Inserts an HTML string into the document. Allows to specify additional options.

```csharp
public void InsertHtml(string html, HtmlInsertOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| html | String | An HTML string to insert into the document. |
| options | HtmlInsertOptions | Options that are used when HTML string is inserted. |

## Remarks

You can use this method to insert an HTML fragment or whole HTML document.

## Examples

Shows how to use options while inserting html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD Name ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD EMAIL ");
builder.InsertParagraph();

// By default "DocumentBuilder.InsertHtml" inserts a HTML fragment that ends with a block-level HTML element,
// it normally closes that block-level element and inserts a paragraph break.
// As a result, a new empty paragraph appears after inserted document.
// If we specify "HtmlInsertOptions.RemoveLastEmptyParagraph", those extra empty paragraphs will be removed.
builder.MoveToMergeField("NAME");
builder.InsertHtml("<p>John Smith</p>", HtmlInsertOptions.UseBuilderFormatting | HtmlInsertOptions.RemoveLastEmptyParagraph);
builder.MoveToMergeField("EMAIL");
builder.InsertHtml("<p>jsmith@example.com</p>", HtmlInsertOptions.UseBuilderFormatting);

doc.Save(ArtifactsDir + "MailMerge.RemoveLastEmptyParagraph.docx");
```

### See Also

* enum [HtmlInsertOptions](../../htmlinsertoptions/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
