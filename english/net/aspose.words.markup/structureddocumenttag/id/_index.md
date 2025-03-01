---
title: StructuredDocumentTag.Id
linktitle: Id
articleTitle: Id
second_title: Aspose.Words for .NET
description: Discover the StructuredDocumentTag Id property, a unique, readonly numerical identifier for efficient SDT management and enhanced document organization.
type: docs
weight: 140
url: /net/aspose.words.markup/structureddocumenttag/id/
---
## StructuredDocumentTag.Id property

Specifies a unique read-only persistent numerical Id for this **SDT**.

```csharp
public int Id { get; }
```

## Remarks

Id attribute shall follow these rules:

* The document shall retain SDT ids only if the whole document is cloned [`Clone`](../../../aspose.words/document/clone/).
* During [`ImportNode`](../../../aspose.words/documentbase/importnode/) Id shall be retained if import does not cause conflicts with other SDT Ids in the target document.
* If multiple SDT nodes specify the same decimal number value for the Id attribute, then the first SDT in the document shall maintain this original Id, and all subsequent SDT nodes shall have new identifiers assigned to them when the document is loaded.
* During standalone SDT INodeCloningListener) operation new unique ID will be generated for the cloned SDT node.
* If Id is not specified in the source document, then the SDT node shall have a new unique identifier assigned to it when the document is loaded.

## Examples

Shows how to create a structured document tag in a plain text box and modify its appearance.

```csharp
Document doc = new Document();

// Create a structured document tag that will contain plain text.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Set the title and color of the frame that appears when you mouse over the structured document tag in Microsoft Word.
tag.Title = "My plain text";
tag.Color = Color.Magenta;

// Set a tag for this structured document tag, which is obtainable
// as an XML element named "tag", with the string below in its "@val" attribute.
tag.Tag = "MyPlainTextSDT";

// Every structured document tag has a random unique ID.
Assert.IsTrue(tag.Id > 0);

// Set the font for the text inside the structured document tag.
tag.ContentsFont.Name = "Arial";

// Set the font for the text at the end of the structured document tag.
// Any text that we type in the document body after moving out of the tag with arrow keys will use this font.
tag.EndCharacterFont.Name = "Arial Black";

// By default, this is false and pressing enter while inside a structured document tag does nothing.
// When set to true, our structured document tag can have multiple lines.

// Set the "Multiline" property to "false" to only allow the contents
// of this structured document tag to span a single line.
// Set the "Multiline" property to "true" to allow the tag to contain multiple lines of content.
tag.Multiline = true;

// Set the "Appearance" property to "SdtAppearance.Tags" to show tags around content.
// By default structured document tag shows as BoundingBox. 
tag.Appearance = SdtAppearance.Tags;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

// Insert a clone of our structured document tag in a new paragraph.
StructuredDocumentTag tagClone = (StructuredDocumentTag)tag.Clone(true);
builder.InsertParagraph();
builder.InsertNode(tagClone);

// Use the "RemoveSelfOnly" method to remove a structured document tag, while keeping its contents in the document.
tagClone.RemoveSelfOnly();

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlainText.docx");
```

### See Also

* class [StructuredDocumentTag](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
