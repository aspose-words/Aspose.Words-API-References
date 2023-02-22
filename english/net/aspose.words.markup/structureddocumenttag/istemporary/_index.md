---
title: IsTemporary
second_title: Aspose.Words for .NET API Reference
description: StructuredDocumentTag property. Specifies whether this SDT shall be removed from the WordProcessingML document when its contents are modified in C#.
type: docs
weight: 160
url: /net/aspose.words.markup/structureddocumenttag/istemporary/
---
## StructuredDocumentTag.IsTemporary property

Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents are modified.

```csharp
public bool IsTemporary { get; set; }
```

## Examples

Shows how to make single-use controls.

```csharp
Document doc = new Document();

// Insert a plain text structured document tag,
// which will act as a plain text form that the user may enter text into.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Set the "IsTemporary" property to "true" to make the structured document tag disappear and
// assimilate its contents into the document after the user edits it once in Microsoft Word.
// Set the "IsTemporary" property to "false" to allow the user to edit the contents
// of the structured document tag any number of times.
tag.IsTemporary = isTemporary;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Please enter text: ");
builder.InsertNode(tag);

// Insert another structured document tag in the form of a check box and set its default state to "checked".
tag = new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline);
tag.Checked = true;

// Set the "IsTemporary" property to "true" to make the check box become a symbol
// once the user clicks on it in Microsoft Word.
// Set the "IsTemporary" property to "false" to allow the user to click on the check box any number of times.
tag.IsTemporary = isTemporary;

builder.Write("\nPlease click the check box: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IsTemporary.docx");
```

### See Also

* class [StructuredDocumentTag](../)
* namespace [Aspose.Words.Markup](../../structureddocumenttag/)
* assembly [Aspose.Words](../../../)
