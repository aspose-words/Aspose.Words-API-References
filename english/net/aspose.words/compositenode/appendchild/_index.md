---
title: CompositeNode.AppendChild
linktitle: AppendChild
articleTitle: AppendChild
second_title: Aspose.Words for .NET
description: Discover how the CompositeNode AppendChild method enhances your coding by seamlessly adding nodes to your child node list. Boost your development efficiency!
type: docs
weight: 80
url: /net/aspose.words/compositenode/appendchild/
---
## CompositeNode.AppendChild&lt;T&gt; method

Adds the specified node to the end of the list of child nodes for this node.

```csharp
public T AppendChild<T>(T newChild)
    where T : Node
```

| Parameter | Type | Description |
| --- | --- | --- |
| newChild | T | The node to add. |

### Return Value

The node added.

## Remarks

If the *newChild* is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use [`ImportNode`](../../documentbase/importnode/) to import the node to the current document. The imported node can then be inserted into the current document.

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

Assert.That(doc.GetText().Trim(), Is.EqualTo("Hello World!"));

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### See Also

* class [Node](../../node/)
* class [CompositeNode](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
