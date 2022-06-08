---
title: CompareOptions
second_title: Aspose.Words for .NET API Reference
description: Allows to choose advanced options for document comparison operation.
type: docs
weight: 260
url: /net/aspose.words.comparing/compareoptions/
---
## CompareOptions class

Allows to choose advanced options for document comparison operation.

```csharp
public class CompareOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [CompareOptions](compareoptions)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [Granularity](../../aspose.words.comparing/compareoptions/granularity) { get; set; } | Specifies whether changes are tracked by character or by word. Default value is WordLevel. |
| [IgnoreCaseChanges](../../aspose.words.comparing/compareoptions/ignorecasechanges) { get; set; } | True indicates that documents comparison is case insensitive. By default comparison is case sensitive. |
| [IgnoreComments](../../aspose.words.comparing/compareoptions/ignorecomments) { get; set; } | Specifies whether to compare differences in comments. By default comments are not ignored. |
| [IgnoreDmlUniqueId](../../aspose.words.comparing/compareoptions/ignoredmluniqueid) { get; set; } | Specifies whether to ignore difference in DrawingML unique Id. Default value is **false**. |
| [IgnoreFields](../../aspose.words.comparing/compareoptions/ignorefields) { get; set; } | Specifies whether to compare differences in fields. By default fields are not ignored. |
| [IgnoreFootnotes](../../aspose.words.comparing/compareoptions/ignorefootnotes) { get; set; } | Specifies whether to compare differences in footnotes and endnotes. By default footnotes are not ignored. |
| [IgnoreFormatting](../../aspose.words.comparing/compareoptions/ignoreformatting) { get; set; } | True indicates that formatting is ignored. By default document formatting is not ignored. |
| [IgnoreHeadersAndFooters](../../aspose.words.comparing/compareoptions/ignoreheadersandfooters) { get; set; } | True indicates that headers and footers content is ignored. By default headers and footers are not ignored. |
| [IgnoreTables](../../aspose.words.comparing/compareoptions/ignoretables) { get; set; } | Specifies whether to compare the differences in data contained in tables. By default tables are not ignored. |
| [IgnoreTextboxes](../../aspose.words.comparing/compareoptions/ignoretextboxes) { get; set; } | Specifies whether to compare differences in the data contained within text boxes. By default textboxes are not ignored. |
| [Target](../../aspose.words.comparing/compareoptions/target) { get; set; } | Specifies which document shall be used as a target during comparison. |

### Examples

Shows how to filter specific types of document elements when making a comparison.

```csharp
// Create the original document and populate it with various kinds of elements.
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);

// Paragraph text referenced with an endnote:
builder.Writeln("Hello world! This is the first paragraph.");
builder.InsertFootnote(FootnoteType.Endnote, "Original endnote text.");

// Table:
builder.StartTable();
builder.InsertCell();
builder.Write("Original cell 1 text");
builder.InsertCell();
builder.Write("Original cell 2 text");
builder.EndTable();

// Textbox:
Shape textBox = builder.InsertShape(ShapeType.TextBox, 150, 20);
builder.MoveTo(textBox.FirstParagraph);
builder.Write("Original textbox contents");

// DATE field:
builder.MoveTo(docOriginal.FirstSection.Body.AppendParagraph(""));
builder.InsertField(" DATE ");

// Comment:
Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", DateTime.Now);
newComment.SetText("Original comment.");
builder.CurrentParagraph.AppendChild(newComment);

// Header:
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Original header contents.");

// Create a clone of our document and perform a quick edit on each of the cloned document's elements.
Document docEdited = (Document)docOriginal.Clone(true);
Paragraph firstParagraph = docEdited.FirstSection.Body.FirstParagraph;

firstParagraph.Runs[0].Text = "hello world! this is the first paragraph, after editing.";
firstParagraph.ParagraphFormat.Style = docEdited.Styles[StyleIdentifier.Heading1];
((Footnote)docEdited.GetChild(NodeType.Footnote, 0, true)).FirstParagraph.Runs[1].Text = "Edited endnote text.";
((Table)docEdited.GetChild(NodeType.Table, 0, true)).FirstRow.Cells[1].FirstParagraph.Runs[0].Text = "Edited Cell 2 contents";
((Shape)docEdited.GetChild(NodeType.Shape, 0, true)).FirstParagraph.Runs[0].Text = "Edited textbox contents";
((FieldDate)docEdited.Range.Fields[0]).UseLunarCalendar = true; 
((Comment)docEdited.GetChild(NodeType.Comment, 0, true)).FirstParagraph.Runs[0].Text = "Edited comment.";
docEdited.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].FirstParagraph.Runs[0].Text =
    "Edited header contents.";

// Comparing documents creates a revision for every edit in the edited document.
// A CompareOptions object has a series of flags that can suppress revisions
// on each respective type of element, effectively ignoring their change.
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.IgnoreFormatting = false;
compareOptions.IgnoreCaseChanges = false;
compareOptions.IgnoreComments = false;
compareOptions.IgnoreTables = false;
compareOptions.IgnoreFields = false;
compareOptions.IgnoreFootnotes = false;
compareOptions.IgnoreTextboxes = false;
compareOptions.IgnoreHeadersAndFooters = false;
compareOptions.Target = ComparisonTargetType.New;

docOriginal.Compare(docEdited, "John Doe", DateTime.Now, compareOptions);
docOriginal.Save(ArtifactsDir + "Document.CompareOptions.docx");
```

### See Also

* namespace [Aspose.Words.Comparing](../../aspose.words.comparing)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
