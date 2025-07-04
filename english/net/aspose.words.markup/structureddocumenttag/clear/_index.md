---
title: StructuredDocumentTag.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words for .NET
description: Effortlessly clear contents of your structured document tag with the Clear method, and show a defined placeholder for enhanced document management.
type: docs
weight: 360
url: /net/aspose.words.markup/structureddocumenttag/clear/
---
## StructuredDocumentTag.Clear method

Clears contents of this structured document tag and displays a placeholder if it is defined.

```csharp
public void Clear()
```

## Remarks

It is not possible to clear contents of a structured document tag if it has revisions.

If this structured document tag is mapped to custom XML (with using the [`XmlMapping`](../xmlmapping/) property), the referenced XML node is cleared.

## Examples

Shows how to delete contents of structured document tag elements.

```csharp
Document doc = new Document();

// Create a plain text structured document tag, and then append it to the document.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// This structured document tag, which is in the form of a text box, already displays placeholder text.
Assert.That(tag.GetText().Trim(), Is.EqualTo("Click here to enter text."));
Assert.That(tag.IsShowingPlaceholderText, Is.True);

// Create a building block with text contents.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;
BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "My placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.EnsureMinimum();
substituteBlock.FirstSection.Body.FirstParagraph.AppendChild(new Run(glossaryDoc, "Custom placeholder text."));
glossaryDoc.AppendChild(substituteBlock);

// Set the structured document tag's "PlaceholderName" property to our building block's name to get
// the structured document tag to display the contents of the building block in place of the original default text.
tag.PlaceholderName = "My placeholder";

Assert.That(tag.GetText().Trim(), Is.EqualTo("Custom placeholder text."));
Assert.That(tag.IsShowingPlaceholderText, Is.True);

// Edit the text of the structured document tag and hide the placeholder text.
Run run = (Run)tag.GetChild(NodeType.Run, 0, true);
run.Text = "New text.";
tag.IsShowingPlaceholderText = false;

Assert.That(tag.GetText().Trim(), Is.EqualTo("New text."));

// Use the "Clear" method to clear this structured document tag's contents and display the placeholder again.
tag.Clear();

Assert.That(tag.IsShowingPlaceholderText, Is.True);
Assert.That(tag.GetText().Trim(), Is.EqualTo("Custom placeholder text."));
```

### See Also

* class [StructuredDocumentTag](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
