---
title: ComparisonTargetType enumeration
linktitle: ComparisonTargetType enumeration
articleTitle: ComparisonTargetType enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Comparing.ComparisonTargetType enumeration. Allows to specify base document which will be used during comparison"
type: docs
weight: 30
url: /nodejs-net/aspose.words.comparing/comparisontargettype/
---

## ComparisonTargetType enumeration

Allows to specify base document which will be used during comparison.  Default value is [ComparisonTargetType.Current](./#Current).


Relates to Microsoft Word "Show changes in" option in "Compare Documents" dialog box.


### Members

| Name | Description |
| --- | --- |
| Current | This document is used as a base during comparison. |
| New | Other document is used as a base during comparison. |

### Examples

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
let compareOptions = new aw.Comparing.CompareOptions
{
  CompareMoves = false,
  IgnoreFormatting = false,
  IgnoreCaseChanges = false,
  IgnoreComments = false,
  IgnoreTables = false,
  IgnoreFields = false,
  IgnoreFootnotes = false,
  IgnoreTextboxes = false,
  IgnoreHeadersAndFooters = false,
  Target = aw.Comparing.ComparisonTargetType.New
};

docOriginal.compare(docEdited, "John Doe", Date.now(), compareOptions);
docOriginal.save(base.artifactsDir + "Revision.compareOptions.docx");
```

### See Also

* module [Aspose.Words.Comparing](../)

