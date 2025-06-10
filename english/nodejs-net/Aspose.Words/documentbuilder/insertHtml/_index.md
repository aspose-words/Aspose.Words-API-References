---
title: DocumentBuilder.insertHtml method
linktitle: insertHtml method
articleTitle: insertHtml method
second_title: Aspose.Words for Node.js
description: "Aspose.Words.DocumentBuilder.insertHtml method"
type: docs
weight: 380
url: /nodejs-net/aspose.words/documentbuilder/insertHtml/
---

## insertHtml(html) {#string}

Inserts an HTML string into the document.


```js
insertHtml(html: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| html | string | An HTML string to insert into the document. |

### Remarks

You can use this method to insert an HTML fragment or whole HTML document.


## insertHtml(html, useBuilderFormatting) {#string_boolean}

Inserts an HTML string into the document.


```js
insertHtml(html: string, useBuilderFormatting: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| html | string | An HTML string to insert into the document. |
| useBuilderFormatting | boolean | A value indicating whether formatting specified in [DocumentBuilder](../) is used as base formatting for text imported from HTML. |

### Remarks

You can use this method to insert an HTML fragment or whole HTML document.

When *useBuilderFormatting* is``false``,
[DocumentBuilder](../) formating is ignored and formatting of inserted text
is based on default HTML formatting. As a result, the text looks as it is rendered in browsers.


When *useBuilderFormatting* is``true``,
formatting of inserted text is based on [DocumentBuilder](../) formatting,
and the text looks as if it were inserted with [DocumentBuilder.write()](../write/#string).





## insertHtml(html, options) {#string_htmlinsertoptions}

Inserts an HTML string into the document. Allows to specify additional options.


```js
insertHtml(html: string, options: Aspose.Words.HtmlInsertOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| html | string | An HTML string to insert into the document. |
| options | [HtmlInsertOptions](../../htmlinsertoptions/) | Options that are used when HTML string is inserted. |

### Remarks

You can use this method to insert an HTML fragment or whole HTML document.


## Examples

Shows how to use a document builder to insert html content into a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

const html = "<p align='right'>Paragraph right</p>" + 
          "<b>Implicit paragraph left</b>" +
          "<div align='center'>Div center</div>" + 
          "<h1 align='left'>Heading 1 left.</h1>";

builder.insertHtml(html);

// Inserting HTML code parses the formatting of each element into equivalent document text formatting.
let paragraphs = doc.firstSection.body.paragraphs;

expect(paragraphs.at(0).getText().trim()).toEqual("Paragraph right");
expect(paragraphs.at(0).paragraphFormat.alignment).toEqual(aw.ParagraphAlignment.Right);

expect(paragraphs.at(1).getText().trim()).toEqual("Implicit paragraph left");
expect(paragraphs.at(1).paragraphFormat.alignment).toEqual(aw.ParagraphAlignment.Left);
expect(paragraphs.at(1).runs.at(0).font.bold).toEqual(true);

expect(paragraphs.at(2).getText().trim()).toEqual("Div center");
expect(paragraphs.at(2).paragraphFormat.alignment).toEqual(aw.ParagraphAlignment.Center);

expect(paragraphs.at(3).getText().trim()).toEqual("Heading 1 left.");
expect(paragraphs.at(3).paragraphFormat.style.name).toEqual("Heading 1");

doc.save(base.artifactsDir + "DocumentBuilder.insertHtml.docx");
```

Shows how to apply a document builder's formatting while inserting HTML content.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Set a text alignment for the builder, insert an HTML paragraph with a specified alignment, and one without.
builder.paragraphFormat.alignment = aw.ParagraphAlignment.Distributed;
builder.insertHtml(
  "<p align='right'>Paragraph 1.</p>" +
  "<p>Paragraph 2.</p>", useBuilderFormatting);

let paragraphs = doc.firstSection.body.paragraphs;

// The first paragraph has an alignment specified. When InsertHtml parses the HTML code,
// the paragraph alignment value found in the HTML code always supersedes the document builder's value.
expect(paragraphs.at(0).getText().trim()).toEqual("Paragraph 1.");
expect(paragraphs.at(0).paragraphFormat.alignment).toEqual(aw.ParagraphAlignment.Right);

// The second paragraph has no alignment specified. It can have its alignment value filled in
// by the builder's value depending on the flag we passed to the InsertHtml method.
expect(paragraphs.at(1).getText().trim()).toEqual("Paragraph 2.");
expect(paragraphs.at(1).paragraphFormat.alignment).toEqual(
  useBuilderFormatting ? aw.ParagraphAlignment.Distributed : aw.ParagraphAlignment.Left);

doc.save(base.artifactsDir + "DocumentBuilder.InsertHtmlWithFormatting.docx");
```

## See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

