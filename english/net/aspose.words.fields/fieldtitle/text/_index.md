---
title: FieldTitle.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: Manage your FieldTitle Text property effortlessly. Easily get or set title text for enhanced clarity and user experience in your application.
type: docs
weight: 20
url: /net/aspose.words.fields/fieldtitle/text/
---
## FieldTitle.Text property

Gets or sets the text of the title.

```csharp
public string Text { get; set; }
```

## Examples

Shows how to use the TITLE field.

```csharp
Document doc = new Document();

// Set a value for the "Title" built-in document property. 
doc.BuiltInDocumentProperties.Title = "My Title";

// We can use the TITLE field to display the value of this property in the document.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldTitle field = (FieldTitle)builder.InsertField(FieldType.FieldTitle, false);
field.Update();

Assert.AreEqual(" TITLE ", field.GetFieldCode());
Assert.AreEqual("My Title", field.Result);

// Setting a value for the field's Text property,
// and then updating the field will also overwrite the corresponding built-in property with the new value.
builder.Writeln();
field = (FieldTitle)builder.InsertField(FieldType.FieldTitle, false);
field.Text = "My New Title";
field.Update();

Assert.AreEqual(" TITLE  \"My New Title\"", field.GetFieldCode());
Assert.AreEqual("My New Title", field.Result);
Assert.AreEqual("My New Title", doc.BuiltInDocumentProperties.Title);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TITLE.docx");
```

### See Also

* class [FieldTitle](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
