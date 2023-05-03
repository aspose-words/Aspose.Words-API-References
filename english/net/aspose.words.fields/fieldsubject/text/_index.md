---
title: FieldSubject.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET API Reference
description: FieldSubject Text property. Gets or sets the text of the subject in C#.
type: docs
weight: 20
url: /net/aspose.words.fields/fieldsubject/text/
---
## FieldSubject.Text property

Gets or sets the text of the subject.

```csharp
public string Text { get; set; }
```

## Examples

Shows how to use the SUBJECT field.

```csharp
Document doc = new Document();

// Set a value for the document's "Subject" built-in property.
doc.BuiltInDocumentProperties.Subject = "My subject";

// Create a SUBJECT field to display the value of that built-in property.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldSubject field = (FieldSubject)builder.InsertField(FieldType.FieldSubject, true);
field.Update();

Assert.AreEqual(" SUBJECT ", field.GetFieldCode());
Assert.AreEqual("My subject", field.Result);

// If we give the SUBJECT field's Text property value and update it, the field will
// overwrite the current value of the "Subject" built-in property with the value of its Text property,
// and then display the new value.
field.Text = "My new subject";
field.Update();

Assert.AreEqual(" SUBJECT  \"My new subject\"", field.GetFieldCode());
Assert.AreEqual("My new subject", field.Result);

Assert.AreEqual("My new subject", doc.BuiltInDocumentProperties.Subject);

doc.Save(ArtifactsDir + "Field.SUBJECT.docx");
```

### See Also

* class [FieldSubject](../)
* namespace [Aspose.Words.Fields](../../fieldsubject/)
* assembly [Aspose.Words](../../../)
