---
title: Aspose::Words::Fields::FieldOptions::get_TemplateName method
linktitle: get_TemplateName
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldOptions::get_TemplateName method. Gets or sets the file name of the template used by the document in C++.'
type: docs
weight: 19000
url: /cpp/aspose.words.fields/fieldoptions/get_templatename/
---
## FieldOptions::get_TemplateName method


Gets or sets the file name of the template used by the document.

```cpp
System::String Aspose::Words::Fields::FieldOptions::get_TemplateName() const
```

## Remarks


This property is used by the [FieldTemplate](../../fieldtemplate/) field if the [AttachedTemplate](../../../aspose.words/document/get_attachedtemplate/) property is empty.

If this property is empty, the default template file name **Normal.dotm** is used.

## Examples



Shows how to use a TEMPLATE field to display the local file system location of a document's template. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// We can set a template name using by the fields. This property is used when the "doc.AttachedTemplate" is empty.
// If this property is empty the default template file name "Normal.dotm" is used.
doc->get_FieldOptions()->set_TemplateName(System::String::Empty);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldTemplate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTemplate, false));
ASSERT_EQ(u" TEMPLATE ", field->GetFieldCode());

builder->Writeln();
field = System::ExplicitCast<Aspose::Words::Fields::FieldTemplate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTemplate, false));
field->set_IncludeFullPath(true);

ASSERT_EQ(u" TEMPLATE  \\p", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TEMPLATE.docx");
```

## See Also

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
