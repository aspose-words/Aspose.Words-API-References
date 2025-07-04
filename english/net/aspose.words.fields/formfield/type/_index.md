---
title: FormField.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: Discover the FormField Type property to easily identify and utilize various form field types, enhancing your web forms' functionality and user experience.
type: docs
weight: 220
url: /net/aspose.words.fields/formfield/type/
---
## FormField.Type property

Returns the form field type.

```csharp
public FieldType Type { get; }
```

## Examples

Shows how to insert a combo box.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Insert a combo box which will allow a user to choose an option from a collection of strings.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.That(comboBox.Name, Is.EqualTo("MyComboBox"));
Assert.That(comboBox.Type, Is.EqualTo(FieldType.FieldFormDropDown));
Assert.That(comboBox.Result, Is.EqualTo("Apple"));

// The form field will appear in the form of a "select" html tag.
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### See Also

* enum [FieldType](../../fieldtype/)
* class [FormField](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
