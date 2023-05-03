---
title: FieldTemplate.IncludeFullPath
linktitle: IncludeFullPath
articleTitle: IncludeFullPath
second_title: Aspose.Words for .NET API Reference
description: FieldTemplate IncludeFullPath property. Gets or sets whether to include the full file path name in C#.
type: docs
weight: 20
url: /net/aspose.words.fields/fieldtemplate/includefullpath/
---
## FieldTemplate.IncludeFullPath property

Gets or sets whether to include the full file path name.

```csharp
public bool IncludeFullPath { get; set; }
```

## Examples

Shows how to use a TEMPLATE field to display the local file system location of a document's template.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// We can set a template name using by the fields. This property is used when the "doc.AttachedTemplate" is empty.
// If this property is empty the default template file name "Normal.dotm" is used.
doc.FieldOptions.TemplateName = string.Empty;

FieldTemplate field = (FieldTemplate)builder.InsertField(FieldType.FieldTemplate, false);
Assert.AreEqual(" TEMPLATE ", field.GetFieldCode());

builder.Writeln();
field = (FieldTemplate)builder.InsertField(FieldType.FieldTemplate, false);
field.IncludeFullPath = true;

Assert.AreEqual(" TEMPLATE  \\p", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TEMPLATE.docx");
```

### See Also

* class [FieldTemplate](../)
* namespace [Aspose.Words.Fields](../../fieldtemplate/)
* assembly [Aspose.Words](../../../)
