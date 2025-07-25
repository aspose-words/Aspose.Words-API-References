---
title: Section
linktitle: Section
articleTitle: Section
second_title: Aspose.Words for .NET
description: Create dynamic web sections effortlessly with our Section Constructor. Easily initialize and customize your Section class for optimal site performance.
type: docs
weight: 10
url: /net/aspose.words/section/section/
---
## Section constructor

Initializes a new instance of the Section class.

```csharp
public Section(DocumentBase doc)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | DocumentBase | The owner document. |

## Remarks

When the section is created, it belongs to the specified document, but is not yet part of the document and [`ParentNode`](../../node/parentnode/) is `null`.

To include [`Section`](../) into a document use [`InsertAfter`](../../compositenode/insertafter/) and [`InsertBefore`](../../compositenode/insertbefore/) methods of the [`Document`](../../document/) OR [`Add`](../../nodecollection/add/) and [`Insert`](../../nodecollection/insert/) methods of the [`Sections`](../../document/sections/) property.

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

* class [DocumentBase](../../documentbase/)
* class [Section](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
