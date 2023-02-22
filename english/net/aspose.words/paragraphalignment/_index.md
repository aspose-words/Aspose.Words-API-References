---
title: ParagraphAlignment Enum
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.ParagraphAlignment enum. Specifies text alignment in a paragraph in C#.
type: docs
weight: 4190
url: /net/aspose.words/paragraphalignment/
---
## ParagraphAlignment enumeration

Specifies text alignment in a paragraph.

```csharp
public enum ParagraphAlignment
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Left | `0` | Text is aligned to the left. |
| Center | `1` | Text is centered horizontally. |
| Right | `2` | Text is aligned to the right. |
| Justify | `3` | Text is aligned to both left and right. |
| Distributed | `4` | Text is evenly distributed. |
| ArabicMediumKashida | `5` | Arabic only. Kashida length for text is extended to a medium length determined by the consumer. |
| ArabicHighKashida | `7` | Arabic only. Kashida length for text is extended to its widest possible length. |
| ArabicLowKashida | `8` | Arabic only. Kashida length for text is extended to a slightly longer length. |
| ThaiDistributed | `9` | Thai only. Text is justified with an optimization for Thai. |
| MathElementCenterAsGroup | `10` | The only Math element in a line, aligned as 'Centered As Group'. |

## Examples

Shows how to construct an Aspose.Words document by hand.

```csharp
Document doc = new Document();

// A blank document contains one section, one body and one paragraph.
// Call the "RemoveAllChildren" method to remove all those nodes,
// and end up with a document node with no children.
doc.RemoveAllChildren();

// This document now has no composite child nodes that we can add content to.
// If we wish to edit it, we will need to repopulate its node collection.
// First, create a new section, and then append it as a child to the root document node.
Section section = new Section(doc);
doc.AppendChild(section);

// Set some page setup properties for the section.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// A section needs a body, which will contain and display all its contents
// on the page between the section's header and footer.
Body body = new Body(doc);
section.AppendChild(body);

// Create a paragraph, set some formatting properties, and then append it as a child to the body.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Finally, add some content to do the document. Create a run,
// set its appearance and contents, and then append it as a child to the paragraph.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
