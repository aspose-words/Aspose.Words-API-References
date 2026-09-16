---
title: "Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat 方法"
linktitle: "get_FieldIndexFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat 方法。获取或设置一个 FieldIndexFormat，用于表示文档中 FieldIndex 字段的格式，在 C++ 中。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.fields/fieldoptions/get_fieldindexformat/
---
## FieldOptions::get_FieldIndexFormat method


获取或设置一个 [FieldIndexFormat](./)，它表示文档中 [FieldIndex](../../fieldindex/) 字段的格式。

```cpp
Aspose::Words::Fields::FieldIndexFormat Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat()
```


## 示例



展示如何格式化 [FieldIndex](../../fieldindex/) 字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"A");
builder->InsertBreak(Aspose::Words::BreakType::LineBreak);
builder->InsertField(u"XE \"A\"");
builder->Write(u"B");

builder->InsertField(u" INDEX \\e \" · \" \\h \"A\" \\c \"2\" \\z \"1033\"", nullptr);

doc->get_FieldOptions()->set_FieldIndexFormat(Aspose::Words::Fields::FieldIndexFormat::Fancy);
doc->UpdateFields();

doc->Save(get_ArtifactsDir() + u"Field.SetFieldIndexFormat.docx");
```

## 另见

* Enum [FieldIndexFormat](../../fieldindexformat/)
* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
