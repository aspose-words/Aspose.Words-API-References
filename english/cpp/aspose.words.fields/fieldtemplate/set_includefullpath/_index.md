---
title: Aspose::Words::Fields::FieldTemplate::set_IncludeFullPath method
linktitle: set_IncludeFullPath
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldTemplate::set_IncludeFullPath method. Sets whether to include the full file path name in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.fields/fieldtemplate/set_includefullpath/
---
## FieldTemplate::set_IncludeFullPath method


Sets whether to include the full file path name.

```cpp
void Aspose::Words::Fields::FieldTemplate::set_IncludeFullPath(bool value)
```

## Examples


Shows how to use a TEMPLATE field to display the local file system location of a document's template.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// We can set a template name using by the fields. This property is used when the "doc.AttachedTemplate" is empty.
// If this property is empty the default template file name "Normal.dotm" is used.
doc->get_FieldOptions()->set_TemplateName(System::String::Empty);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldTemplate>(builder->InsertField(FieldType::FieldTemplate, false));
ASSERT_EQ(u" TEMPLATE ", field->GetFieldCode());

builder->Writeln();
field = System::ExplicitCast<Aspose::Words::Fields::FieldTemplate>(builder->InsertField(FieldType::FieldTemplate, false));
field->set_IncludeFullPath(true);

ASSERT_EQ(u" TEMPLATE  \\p", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TEMPLATE.docx");
```
## See Also

* Class [FieldTemplate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
