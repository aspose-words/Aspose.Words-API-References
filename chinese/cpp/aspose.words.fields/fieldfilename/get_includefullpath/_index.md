---
title: "Aspose::Words::Fields::FieldFileName::get_IncludeFullPath 方法"
linktitle: "get_IncludeFullPath"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldFileName::get_IncludeFullPath 方法。获取或设置在 C++ 中是否包含完整的文件路径名称。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fieldfilename/get_includefullpath/
---
## FieldFileName::get_IncludeFullPath method


获取或设置是否包含完整的文件路径名称。

```cpp
bool Aspose::Words::Fields::FieldFileName::get_IncludeFullPath()
```


## 示例



展示如何使用 [FieldOptions](../../fieldoptions/) 来覆盖 FILENAME 字段的默认值。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToDocumentEnd();
builder->Writeln();

// 此 FILENAME 字段将显示我们加载的文档的本地系统文件名。
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldFileName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileName, true));
field->Update();

ASSERT_EQ(u" FILENAME ", field->GetFieldCode());
ASSERT_EQ(u"Document.docx", field->get_Result());

builder->Writeln();

// 默认情况下，FILENAME 字段显示文件的名称，但不显示其完整的本地文件系统路径。
// 我们可以设置一个标志，使其显示完整的文件路径。
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileName, true));
field->set_IncludeFullPath(true);
field->Update();

ASSERT_EQ(get_MyDir() + u"Document.docx", field->get_Result());

// 我们也可以为此属性设置一个值，以
// 覆盖 FILENAME 字段显示的值。
doc->get_FieldOptions()->set_FileName(u"FieldOptions.FILENAME.docx");
field->Update();

ASSERT_EQ(u" FILENAME  \\p", field->GetFieldCode());
ASSERT_EQ(u"FieldOptions.FILENAME.docx", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + doc->get_FieldOptions()->get_FileName());
```

## 另见

* Class [FieldFileName](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
