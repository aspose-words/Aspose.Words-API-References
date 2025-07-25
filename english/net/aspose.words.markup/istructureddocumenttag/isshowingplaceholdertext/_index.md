---
title: IStructuredDocumentTag.IsShowingPlaceholderText
linktitle: IsShowingPlaceholderText
articleTitle: IsShowingPlaceholderText
second_title: Aspose.Words for .NET
description: Discover the IStructuredDocumentTag IsShowingPlaceholderText property to easily identify placeholder text in your SDT, enhancing content clarity and management.
type: docs
weight: 50
url: /net/aspose.words.markup/istructureddocumenttag/isshowingplaceholdertext/
---
## IStructuredDocumentTag.IsShowingPlaceholderText property

Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT).

if set to true, this state shall be resumed (showing placeholder text) upon opening this document.

```csharp
public bool IsShowingPlaceholderText { get; set; }
```

## Examples

Shows how to use a building block's contents as a custom placeholder text for a structured document tag.

```csharp
Document doc = new Document();

// Insert a plain text structured document tag of the "PlainText" type, which will function as a text box.
// The contents that it will display by default are a "Click here to enter text." prompt.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// We can get the tag to display the contents of a building block instead of the default text.
// First, add a building block with contents to the glossary document.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;

BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "Custom Placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.AppendChild(new Body(glossaryDoc));
substituteBlock.FirstSection.Body.AppendParagraph("Custom placeholder text.");

glossaryDoc.AppendChild(substituteBlock);

// Then, use the structured document tag's "PlaceholderName" property to reference that building block by name.
tag.PlaceholderName = "Custom Placeholder";

// If "PlaceholderName" refers to an existing block in the parent document's glossary document,
// we will be able to verify the building block via the "Placeholder" property.
Assert.That(tag.Placeholder, Is.EqualTo(substituteBlock));

// Set the "IsShowingPlaceholderText" property to "true" to treat the
// structured document tag's current contents as placeholder text.
// This means that clicking on the text box in Microsoft Word will immediately highlight all the tag's contents.
// Set the "IsShowingPlaceholderText" property to "false" to get the
// structured document tag to treat its contents as text that a user has already entered.
// Clicking on this text in Microsoft Word will place the blinking cursor at the clicked location.
tag.IsShowingPlaceholderText = isShowingPlaceholderText;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

### See Also

* interface [IStructuredDocumentTag](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
