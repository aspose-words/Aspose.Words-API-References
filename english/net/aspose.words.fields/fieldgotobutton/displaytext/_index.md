---
title: FieldGoToButton.DisplayText
linktitle: DisplayText
articleTitle: DisplayText
second_title: Aspose.Words for .NET
description: Customize your FieldGoToButton's DisplayText property to enhance user experience. Easily set button text for seamless document navigation and quick access.
type: docs
weight: 20
url: /net/aspose.words.fields/fieldgotobutton/displaytext/
---
## FieldGoToButton.DisplayText property

Gets or sets the text of the "button" that appears in the document, such that it can be selected to activate the jump.

```csharp
public string DisplayText { get; set; }
```

## Examples

Shows to insert a GOTOBUTTON field.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Add a GOTOBUTTON field. When we double-click this field in Microsoft Word,
// it will take the text cursor to the bookmark whose name the Location property references.
FieldGoToButton field = (FieldGoToButton)builder.InsertField(FieldType.FieldGoToButton, true);
field.DisplayText = "My Button";
field.Location = "MyBookmark";

Assert.That(field.GetFieldCode(), Is.EqualTo(" GOTOBUTTON  MyBookmark My Button"));

// Insert a valid bookmark for the field to reference.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark(field.Location);
builder.Writeln("Bookmark text contents.");
builder.EndBookmark(field.Location);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.GOTOBUTTON.docx");
```

### See Also

* class [FieldGoToButton](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
