---
title: get_IncludeFullPath
second_title: Aspose.Words for C++ API Reference
description: Gets or sets whether to include the full file path name.
type: docs
weight: 1
url: /cpp/aspose.words.fields/fieldtemplate/get_includefullpath/
---
## FieldTemplate::get_IncludeFullPath method


Gets or sets whether to include the full file path name.

```cpp
bool Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath()
```


## Examples



Shows how to use a TEMPLATE field to display the local file system location of a document's template. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// We can set a template name using by the fields. This property is used when the "doc.AttachedTemplate" is empty.
// If this property is empty the default template file name "Normal.dotm" is used.
doc->get_FieldOptions()->set_TemplateName(String::Empty);

auto field = System::DynamicCast<FieldTemplate>(builder->InsertField(FieldType::FieldTemplate, false));
ASSERT_EQ(u" TEMPLATE ", field->GetFieldCode());

builder->Writeln();
field = System::DynamicCast<FieldTemplate>(builder->InsertField(FieldType::FieldTemplate, false));
field->set_IncludeFullPath(true);

ASSERT_EQ(u" TEMPLATE  \\p", field->GetFieldCode());

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.TEMPLATE.docx");
```

## See Also

* Class [FieldTemplate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
