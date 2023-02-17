---
title: FormField.Name
second_title: Aspose.Words for .NET API Reference
description: FormField property. Gets or sets the form field name in C#.
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

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// The form field will appear in the form of a "select" html tag.
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### See Also

* class [FormField](../)
* namespace [Aspose.Words.Fields](../../formfield/)
* assembly [Aspose.Words](../../../)
