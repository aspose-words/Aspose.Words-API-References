---
title: StructuredDocumentTag.Tag
linktitle: Tag
second_title: Aspose.Words for .NET API Reference
description: StructuredDocumentTag property. Specifies a tag associated with the current SDT node. Can not be null in C#.
type: docs
weight: 280
url: /net/aspose.words.markup/structureddocumenttag/tag/
---
## StructuredDocumentTag.Tag property

Specifies a tag associated with the current SDT node. Can not be `null`.

```csharp
public string Tag { get; set; }
```

## Remarks

A tag is an arbitrary string which applications can associate with SDT in order to identify it without providing a visible friendly name.

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
Assert.That(tag.Id, Is.Positive);

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
* namespace [Aspose.Words.Markup](../../structureddocumenttag/)
* assembly [Aspose.Words](../../../)
