---
title: FormField.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words for .NET
description: Discover how to easily manage the FormField Name property to customize and optimize your forms for better user engagement and data collection.
type: docs
weight: 130
url: /net/aspose.words.fields/formfield/name/
---
## FormField.Name property

Gets or sets the form field name.

```csharp
public string Name { get; set; }
```

## Remarks

Microsoft Word allows strings with at most 20 characters.

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

* class [FormField](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
