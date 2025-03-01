---
title: FieldInfo.NewValue
linktitle: NewValue
articleTitle: NewValue
second_title: Aspose.Words for .NET
description: Discover the FieldInfo NewValue property, easily manage optional values to enhance your data updates and streamline your coding experience.
type: docs
weight: 30
url: /net/aspose.words.fields/fieldinfo/newvalue/
---
## FieldInfo.NewValue property

Gets or sets an optional value that updates the property.

```csharp
public string NewValue { get; set; }
```

## Examples

Shows how to work with INFO fields.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Set a value for the "Comments" built-in property and then insert an INFO field to display that property's value.
doc.BuiltInDocumentProperties.Comments = "My comment";
FieldInfo field = (FieldInfo)builder.InsertField(FieldType.FieldInfo, true);
field.InfoType = "Comments";
field.Update();

Assert.AreEqual(" INFO  Comments", field.GetFieldCode());
Assert.AreEqual("My comment", field.Result);

builder.Writeln();

// Setting a value for the field's NewValue property and updating
// the field will also overwrite the corresponding built-in property with the new value.
field = (FieldInfo)builder.InsertField(FieldType.FieldInfo, true);
field.InfoType = "Comments";
field.NewValue = "New comment";
field.Update();

Assert.AreEqual(" INFO  Comments \"New comment\"", field.GetFieldCode());
Assert.AreEqual("New comment", field.Result);
Assert.AreEqual("New comment", doc.BuiltInDocumentProperties.Comments);

doc.Save(ArtifactsDir + "Field.INFO.docx");
```

### See Also

* class [FieldInfo](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
