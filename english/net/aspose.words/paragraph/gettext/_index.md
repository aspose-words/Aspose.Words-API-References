---
title: Paragraph.GetText
linktitle: GetText
articleTitle: GetText
second_title: Aspose.Words for .NET
description: Discover the Paragraph GetText method to effortlessly retrieve text, including paragraph endings, enhancing your text processing efficiency.
type: docs
weight: 280
url: /net/aspose.words/paragraph/gettext/
---
## Paragraph.GetText method

Gets the text of this paragraph including the end of paragraph character.

```csharp
public override string GetText()
```

## Remarks

The text of all child nodes is concatenated and the end of paragraph character is appended as follows:

* If the paragraph is the last paragraph of [`Body`](../../body/), then [`SectionBreak`](../../controlchar/sectionbreak/) (\x000c) is appended.
* If the paragraph is the last paragraph of [`Cell`](../../../aspose.words.tables/cell/), then [`Cell`](../../controlchar/cell/) (\x0007) is appended.
* For all other paragraphs [`ParagraphBreak`](../../controlchar/paragraphbreak/) (\r) is appended.

The returned string includes all control and special characters as described in [`ControlChar`](../../controlchar/).

## Examples

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```csharp
Document doc = new Document();

// An empty document, by default, has one paragraph.
Assert.That(doc.FirstSection.Body.Paragraphs.Count, Is.EqualTo(1));

// Composite nodes such as our paragraph can contain other composite and inline nodes as children.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Create three more run nodes.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// The document body will not display these runs until we insert them into a composite node
// that itself is a part of the document's node tree, as we did with the first run.
// We can determine where the text contents of nodes that we insert
// appears in the document by specifying an insertion location relative to another node in the paragraph.
Assert.That(paragraph.GetText().Trim(), Is.EqualTo("Initial text."));

// Insert the second run into the paragraph in front of the initial run.
paragraph.InsertBefore(run2, paragraphText);

Assert.That(paragraph.GetText().Trim(), Is.EqualTo("Run 2. Initial text."));

// Insert the third run after the initial run.
paragraph.InsertAfter(run3, paragraphText);

Assert.That(paragraph.GetText().Trim(), Is.EqualTo("Run 2. Initial text. Run 3."));

// Insert the first run to the start of the paragraph's child nodes collection.
paragraph.PrependChild(run1);

Assert.That(paragraph.GetText().Trim(), Is.EqualTo("Run 1. Run 2. Initial text. Run 3."));
Assert.That(paragraph.GetChildNodes(NodeType.Any, true).Count, Is.EqualTo(4));

// We can modify the contents of the run by editing and deleting existing child nodes.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.That(paragraph.GetText().Trim(), Is.EqualTo("Run 1. Updated run 2. Run 3."));
Assert.That(paragraph.GetChildNodes(NodeType.Any, true).Count, Is.EqualTo(3));
```

### See Also

* class [Paragraph](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
