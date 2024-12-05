---
title: ControlChar Class
linktitle: ControlChar
articleTitle: ControlChar
second_title: Aspose.Words for .NET
description: Aspose.Words.ControlChar class. Control characters often encountered in documents in C#.
type: docs
weight: 530
url: /net/aspose.words/controlchar/
---
## ControlChar class

Control characters often encountered in documents.

To learn more, visit the [Working With Control Characters](https://docs.aspose.com/words/net/working-with-control-characters/) documentation article.

```csharp
public static class ControlChar
```

## Fields

| Name | Description |
| --- | --- |
| static readonly [Cell](../../aspose.words/controlchar/cell/) | End of a table cell or end of a table row character: "\x0007" or "\a". |
| const [CellChar](../../aspose.words/controlchar/cellchar/) | End of a table cell or end of a table row character: (char)7 or "\a". |
| static readonly [ColumnBreak](../../aspose.words/controlchar/columnbreak/) | End of column character: "\x000e". |
| const [ColumnBreakChar](../../aspose.words/controlchar/columnbreakchar/) | End of column character: (char)14. |
| static readonly [Cr](../../aspose.words/controlchar/cr/) | Carriage return character: "\x000d" or "\r". Same as [`ParagraphBreak`](./paragraphbreak/). |
| static readonly [CrLf](../../aspose.words/controlchar/crlf/) | Carriage return followed by line feed character: "\x000d\x000a" or "\r\n". Not used as such in Microsoft Word documents, but commonly used in text files for paragraph breaks. |
| const [DefaultTextInputChar](../../aspose.words/controlchar/defaulttextinputchar/) | This is the "o" character used as a default value in text input form fields. |
| const [FieldEndChar](../../aspose.words/controlchar/fieldendchar/) | End of MS Word field character: (char)21. |
| const [FieldSeparatorChar](../../aspose.words/controlchar/fieldseparatorchar/) | Field separator character separates field code from field value. Optional in some fields. Value: (char)20. |
| const [FieldStartChar](../../aspose.words/controlchar/fieldstartchar/) | Start of MS Word field character: (char)19. |
| static readonly [Lf](../../aspose.words/controlchar/lf/) | Line feed character: "\x000a" or "\n". Same as [`LineFeed`](./linefeed/). |
| static readonly [LineBreak](../../aspose.words/controlchar/linebreak/) | Line break character: "\x000b" or "\v". |
| const [LineBreakChar](../../aspose.words/controlchar/linebreakchar/) | Line break character: (char)11 or "\v". |
| static readonly [LineFeed](../../aspose.words/controlchar/linefeed/) | Line feed character: "\x000a" or "\n". Same as [`Lf`](./lf/). |
| const [LineFeedChar](../../aspose.words/controlchar/linefeedchar/) | Line feed character: (char)10 or "\n". |
| const [NonBreakingHyphenChar](../../aspose.words/controlchar/nonbreakinghyphenchar/) | Non-breaking Hyphen in Microsoft Word is (char)30. |
| static readonly [NonBreakingSpace](../../aspose.words/controlchar/nonbreakingspace/) | Non-breaking space character: "\x00a0". |
| const [NonBreakingSpaceChar](../../aspose.words/controlchar/nonbreakingspacechar/) | Non-breaking space character: (char)160. |
| const [OptionalHyphenChar](../../aspose.words/controlchar/optionalhyphenchar/) | Optional Hyphen in Microsoft Word is (char)31. |
| static readonly [PageBreak](../../aspose.words/controlchar/pagebreak/) | Page break character: "\x000c" or "\f". Note it has the same value as [`SectionBreak`](./sectionbreak/). |
| const [PageBreakChar](../../aspose.words/controlchar/pagebreakchar/) | Page break character: (char)12 or "\f". |
| static readonly [ParagraphBreak](../../aspose.words/controlchar/paragraphbreak/) | End of paragraph character: "\x000d" or "\r". Same as [`Cr`](./cr/) |
| const [ParagraphBreakChar](../../aspose.words/controlchar/paragraphbreakchar/) | End of paragraph character: (char)13 or "\r". |
| static readonly [SectionBreak](../../aspose.words/controlchar/sectionbreak/) | End of section character: "\x000c" or "\f". Note it has the same value as [`PageBreak`](./pagebreak/). |
| const [SectionBreakChar](../../aspose.words/controlchar/sectionbreakchar/) | End of section character: (char)12 or "\f". |
| const [SpaceChar](../../aspose.words/controlchar/spacechar/) | Space character: (char)32. |
| static readonly [Tab](../../aspose.words/controlchar/tab/) | Tab character: "\x0009" or "\t". |
| const [TabChar](../../aspose.words/controlchar/tabchar/) | Tab character: (char)9 or "\t". |

## Remarks

Provides both char and string versions of the same constants. For example: string [`LineBreak`](./linebreak/) and char [`LineBreakChar`](./linebreakchar/) have the same value.

## Examples

Shows how to use control characters.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert paragraphs with text with DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Converting the document to text form reveals that control characters
// represent some of the document's structural elements, such as page breaks.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// When converting a document to string form,
// we can omit some of the control characters with the Trim method.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
