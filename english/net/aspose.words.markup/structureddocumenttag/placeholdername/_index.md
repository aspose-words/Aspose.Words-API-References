---
title: StructuredDocumentTag.PlaceholderName
linktitle: PlaceholderName
articleTitle: PlaceholderName
second_title: Aspose.Words for .NET
description: Discover the StructuredDocumentTag PlaceholderName property to easily manage BuildingBlock names and enhance your document's placeholder text.
type: docs
weight: 240
url: /net/aspose.words.markup/structureddocumenttag/placeholdername/
---
## StructuredDocumentTag.PlaceholderName property

Gets or sets Name of the [`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/) containing placeholder text.

```csharp
public string PlaceholderName { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| InvalidOperationException | Throw if BuildingBlock with this name [`Name`](../../../aspose.words.buildingblocks/buildingblock/name/) is not present in [`GlossaryDocument`](../../../aspose.words/document/glossarydocument/). |

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

* class [StructuredDocumentTag](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
