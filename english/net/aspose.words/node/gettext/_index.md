---
title: Node.GetText
linktitle: GetText
articleTitle: GetText
second_title: Aspose.Words for .NET
description: Discover the Node GetText method to effortlessly retrieve text from a node and its child elements, enhancing your data management and development efficiency.
type: docs
weight: 120
url: /net/aspose.words/node/gettext/
---
## Node.GetText method

Gets the text of this node and of all its children.

```csharp
public virtual string GetText()
```

## Remarks

The returned string includes all control and special characters as described in [`ControlChar`](../../controlchar/).

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
Assert.That(doc.GetText(), Is.EqualTo($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak));

// When converting a document to string form,
// we can omit some of the control characters with the Trim method.
Assert.That(doc.GetText().Trim(), Is.EqualTo($"Hello world!{ControlChar.Cr}" +
                "Hello again!"));
```

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

Assert.That(doc.GetText().Trim(), Is.EqualTo("Hello World!"));

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### See Also

* class [Node](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
