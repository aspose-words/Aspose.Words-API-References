---
title: FieldSubject.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: Manage the FieldSubject Text property effortlessly—get or set your subject text for seamless data handling and enhanced user experience.
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

Assert.That(field.GetFieldCode(), Is.EqualTo(" SUBJECT "));
Assert.That(field.Result, Is.EqualTo("My subject"));

// If we give the SUBJECT field's Text property value and update it, the field will
// overwrite the current value of the "Subject" built-in property with the value of its Text property,
// and then display the new value.
field.Text = "My new subject";
field.Update();

Assert.That(field.GetFieldCode(), Is.EqualTo(" SUBJECT  \"My new subject\""));
Assert.That(field.Result, Is.EqualTo("My new subject"));

Assert.That(doc.BuiltInDocumentProperties.Subject, Is.EqualTo("My new subject"));

doc.Save(ArtifactsDir + "Field.SUBJECT.docx");
```

### See Also

* class [FieldSubject](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
