---
title: FieldComments.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: Manage your comments effortlessly with the FieldComments Text property—easily get or set comment text for enhanced user interaction.
type: docs
weight: 20
url: /net/aspose.words.fields/fieldcomments/text/
---
## FieldComments.Text property

Gets or sets the text of the comments.

```csharp
public string Text { get; set; }
```

## Examples

Shows how to use the COMMENTS field.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Set a value for the document's "Comments" built-in property.
doc.BuiltInDocumentProperties.Comments = "My comment.";

// Create a COMMENTS field to display the value of that built-in property.
FieldComments field = (FieldComments)builder.InsertField(FieldType.FieldComments, true);
field.Update();

Assert.AreEqual(" COMMENTS ", field.GetFieldCode());
Assert.AreEqual("My comment.", field.Result);

// If we give the COMMENTS field's Text property value and update it, the field will
// overwrite the current value of the "Comments" built-in property with the value of its Text property,
// and then display the new value.
field.Text = "My overriding comment.";
field.Update();

Assert.AreEqual(" COMMENTS  \"My overriding comment.\"", field.GetFieldCode());
Assert.AreEqual("My overriding comment.", field.Result);

doc.Save(ArtifactsDir + "Field.COMMENTS.docx");
```

### See Also

* class [FieldComments](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
