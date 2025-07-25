---
title: FieldDocVariable.VariableName
linktitle: VariableName
articleTitle: VariableName
second_title: Aspose.Words for .NET
description: Discover the FieldDocVariable VariableName property to easily manage document variables. Simplify retrieval and enhance your document management today!
type: docs
weight: 20
url: /net/aspose.words.fields/fielddocvariable/variablename/
---
## FieldDocVariable.VariableName property

Gets or sets the name of the document variable to retrieve.

```csharp
public string VariableName { get; set; }
```

## Examples

Shows how to use DOCPROPERTY fields to display document properties and variables.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Below are two ways of using DOCPROPERTY fields.
// 1 -  Display a built-in property:
// Set a custom value for the "Category" built-in property, then insert a DOCPROPERTY field that references it.
doc.BuiltInDocumentProperties.Category = "My category";

FieldDocProperty fieldDocProperty = (FieldDocProperty)builder.InsertField(" DOCPROPERTY Category ");
fieldDocProperty.Update();

Assert.That(fieldDocProperty.GetFieldCode(), Is.EqualTo(" DOCPROPERTY Category "));
Assert.That(fieldDocProperty.Result, Is.EqualTo("My category"));

builder.InsertParagraph();

// 2 -  Display a custom document variable:
// Define a custom variable, then reference that variable with a DOCPROPERTY field.
Assert.That(doc.Variables.Count, Is.EqualTo(0));
doc.Variables.Add("My variable", "My variable's value");

FieldDocVariable fieldDocVariable = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
fieldDocVariable.VariableName = "My Variable";
fieldDocVariable.Update();

Assert.That(fieldDocVariable.GetFieldCode(), Is.EqualTo(" DOCVARIABLE  \"My Variable\""));
Assert.That(fieldDocVariable.Result, Is.EqualTo("My variable's value"));

doc.Save(ArtifactsDir + "Field.DOCPROPERTY.DOCVARIABLE.docx");
```

### See Also

* class [FieldDocVariable](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
