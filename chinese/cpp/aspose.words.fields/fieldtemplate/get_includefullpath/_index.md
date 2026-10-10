---
title: "Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath 方法"
linktitle: "get_IncludeFullPath"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath 方法。获取或设置是否在 C++ 中包含完整的文件路径名称。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fieldtemplate/get_includefullpath/
---
## FieldTemplate::get_IncludeFullPath method


获取或设置是否包含完整的文件路径名称。

```cpp
bool Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath()
```


## 示例



展示如何使用 TEMPLATE 字段显示文档模板的本地文件系统位置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 我们可以通过字段设置模板名称。当 "doc.AttachedTemplate" 为空时使用此属性。
// 如果此属性为空，将使用默认模板文件名 "Normal.dotm"。
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

## 另见

* Class [FieldTemplate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
