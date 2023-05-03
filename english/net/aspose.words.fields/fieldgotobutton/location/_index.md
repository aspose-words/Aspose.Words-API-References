---
title: FieldGoToButton.Location
linktitle: Location
articleTitle: Location
second_title: Aspose.Words for .NET API Reference
description: FieldGoToButton Location property. Gets or sets the name of a bookmark a page number or some other item to jump to in C#.
type: docs
weight: 30
url: /net/aspose.words.fields/fieldgotobutton/location/
---
## FieldGoToButton.Location property

Gets or sets the name of a bookmark, a page number, or some other item to jump to.

```csharp
public string Location { get; set; }
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

Assert.AreEqual(" GOTOBUTTON  MyBookmark My Button", field.GetFieldCode());

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
* namespace [Aspose.Words.Fields](../../fieldgotobutton/)
* assembly [Aspose.Words](../../../)
