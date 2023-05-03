---
title: Section.Body
linktitle: Body
second_title: Aspose.Words for .NET API Reference
description: Section Body property. Returns the Body child node of the section in C#.
type: docs
weight: 20
url: /net/aspose.words/section/body/
---
## Section.Body property

Returns the [`Body`](../../body/) child node of the section.

```csharp
public Body Body { get; }
```

## Remarks

[`Body`](../../body/) contains main text of the section.

Returns `null` if the section does not have a [`Body`](../../body/) node among its children.

## Examples

Clears main text from all sections from the document leaving the sections themselves.

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

// A section needs a body, which will contain and display all its contents
// on the page between the section's header and footer.
Body body = new Body(doc);
section.AppendChild(body);

// This body has no children, so we cannot add runs to it yet.
Assert.AreEqual(0, doc.FirstSection.Body.GetChildNodes(NodeType.Any, true).Count);

// Call the "EnsureMinimum" to make sure that this body contains at least one empty paragraph. 
body.EnsureMinimum();

// Now, we can add runs to the body, and get the document to display them.
body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### See Also

* class [Body](../../body/)
* class [Section](../)
* namespace [Aspose.Words](../../section/)
* assembly [Aspose.Words](../../../)
