---
title: Document.compare method
linktitle: compare method
articleTitle: compare method
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Document.compare method"
type: docs
weight: 580
url: /nodejs-net/aspose.words/document/compare/
---

## compare(document, author, dateTime) {#document_string_date}

Compares this document with another document producing changes as number of edit and format revisions [Revision](../../revision/).



```js
compare(document: Aspose.Words.Document, author: string, dateTime: Date)
```

| Parameter | Type | Description |
| --- | --- | --- |
| document | [Document](../) | Document to compare. |
| author | string | Initials of the author to use for revisions. |
| dateTime | Date | The date and time to use for revisions. |

### Remarks

> **NOTE**
>
> Documents must not have revisions before comparison.




## compare(document, author, dateTime, options) {#document_string_date_compareoptions}

Compares this document with another document producing changes as a number of edit and format revisions [Revision](../../revision/).
Allows to specify comparison options using [CompareOptions](../../../aspose.words.comparing/compareoptions/).



```js
compare(document: Aspose.Words.Document, author: string, dateTime: Date, options: Aspose.Words.Comparing.CompareOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| document | [Document](../) |  |
| author | string |  |
| dateTime | Date |  |
| options | [CompareOptions](../../../aspose.words.comparing/compareoptions/) |  |

## Examples

Shows how to compare documents.

```js
let docOriginal = new aw.Document();
let builder = new aw.DocumentBuilder(docOriginal);
builder.writeln("This is the original document.");

let docEdited = new aw.Document();
builder = new aw.DocumentBuilder(docEdited);
builder.writeln("This is the edited document.");

// Comparing documents with revisions will throw an exception.
if (docOriginal.revisions.count == 0 && docEdited.revisions.count == 0)
  docOriginal.compare(docEdited, "authorName", Date.now());

// After the comparison, the original document will gain a new revision
// for every element that is different in the edited document.
expect(docOriginal.revisions.count).toEqual(2);
for (let r of docOriginal.revisions)
{
  console.log(`Revision type: ${r.revisionType}, on a node of type \"${r.parentNode.nodeType}\"`);
  console.log(`\tChanged text: \"${r.parentNode.getText()}\"`);
}

// Accepting these revisions will transform the original document into the edited document.
docOriginal.revisions.acceptAll();

expect(docEdited.getText()).toEqual(docOriginal.getText());
```

Shows how to filter specific types of document elements when making a comparison.

```js
// Create the original document and populate it with various kinds of elements.
let docOriginal = new aw.Document();
let builder = new aw.DocumentBuilder(docOriginal);

// Paragraph text referenced with an endnote:
builder.writeln("Hello world! This is the first paragraph.");
builder.insertFootnote(aw.Notes.FootnoteType.Endnote, "Original endnote text.");

// Table:
builder.startTable();
builder.insertCell();
builder.write("Original cell 1 text");
builder.insertCell();
builder.write("Original cell 2 text");
builder.endTable();

// Textbox:
let textBox = builder.insertShape(aw.Drawing.ShapeType.TextBox, 150, 20);
builder.moveTo(textBox.firstParagraph);
builder.write("Original textbox contents");

// DATE field:
builder.moveTo(docOriginal.firstSection.body.appendParagraph(""));
builder.insertField(" DATE ");

// Comment:
let newComment = new aw.Comment(docOriginal, "John Doe", "J.D.", Date.now());
newComment.setText("Original comment.");
builder.currentParagraph.appendChild(newComment);

// Header:
builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderPrimary);
builder.writeln("Original header contents.");

// Create a clone of our document and perform a quick edit on each of the cloned document's elements.
let docEdited = (Document)docOriginal.clone(true);
let firstParagraph = docEdited.firstSection.body.firstParagraph;

firstParagraph.runs.at(0).text = "hello world! this is the first paragraph, after editing.";
firstParagraph.paragraphFormat.style = docEdited.styles.at(aw.StyleIdentifier.Heading1);
((Footnote)docEdited.getChild(aw.NodeType.Footnote, 0, true)).FirstParagraph.runs.at(1).text = "Edited endnote text.";
((Table)docEdited.getChild(aw.NodeType.Table, 0, true)).FirstRow.cells.at(1).firstParagraph.runs.at(0).text = "Edited Cell 2 contents";
((Shape)docEdited.getShape(0, true)).FirstParagraph.runs.at(0).text = "Edited textbox contents";
((FieldDate)docEdited.range.fields.at(0)).UseLunarCalendar = true;
((Comment)docEdited.getChild(aw.NodeType.Comment, 0, true)).FirstParagraph.runs.at(0).text = "Edited comment.";
docEdited.firstSection.headersFooters.getByHeaderFooterType(aw.HeaderFooterType.HeaderPrimary).firstParagraph.runs.at(0).text =
  "Edited header contents.";

// Comparing documents creates a revision for every edit in the edited document.
// A CompareOptions object has a series of flags that can suppress revisions
// on each respective type of element, effectively ignoring their change.
Aspose.words.Comparing.CompareOptions compareOptions = new Aspose.words.Comparing.CompareOptions();
compareOptions.ignoreFormatting = false;
compareOptions.ignoreCaseChanges = false;
compareOptions.ignoreComments = false;
compareOptions.ignoreTables = false;
compareOptions.ignoreFields = false;
compareOptions.ignoreFootnotes = false;
compareOptions.ignoreTextboxes = false;
compareOptions.ignoreHeadersAndFooters = false;
compareOptions.target = aw.Comparing.ComparisonTargetType.New;

docOriginal.compare(docEdited, "John Doe", Date.now(), compareOptions);
docOriginal.save(base.artifactsDir + "Document.CompareOptions.docx");
```

## See Also

* module [Aspose.Words](../../)
* class [Document](../)

