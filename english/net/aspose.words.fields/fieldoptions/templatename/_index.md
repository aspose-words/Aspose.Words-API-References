---
title: FieldOptions.TemplateName
linktitle: TemplateName
articleTitle: TemplateName
second_title: Aspose.Words for .NET
description: Discover the FieldOptions TemplateName property to easily manage your document's template file name for enhanced organization and efficiency.
type: docs
weight: 190
url: /net/aspose.words.fields/fieldoptions/templatename/
---
## FieldOptions.TemplateName property

Gets or sets the file name of the template used by the document.

```csharp
public string TemplateName { get; set; }
```

## Remarks

This property is used by the [`FieldTemplate`](../../fieldtemplate/) field if the [`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) property is empty.

If this property is empty, the default template file name `Normal.dotm` is used.

## Examples

Shows how to use a TEMPLATE field to display the local file system location of a document's template.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// We can set a template name using by the fields. This property is used when the "doc.AttachedTemplate" is empty.
// If this property is empty the default template file name "Normal.dotm" is used.
doc.FieldOptions.TemplateName = string.Empty;

FieldTemplate field = (FieldTemplate)builder.InsertField(FieldType.FieldTemplate, false);
Assert.That(field.GetFieldCode(), Is.EqualTo(" TEMPLATE "));

builder.Writeln();
field = (FieldTemplate)builder.InsertField(FieldType.FieldTemplate, false);
field.IncludeFullPath = true;

Assert.That(field.GetFieldCode(), Is.EqualTo(" TEMPLATE  \\p"));

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TEMPLATE.docx");
```

### See Also

* class [FieldOptions](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
