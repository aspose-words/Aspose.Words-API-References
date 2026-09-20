---
title: "Aspose::Words::Fields::FieldTitle::get_Text 方法"
linktitle: "get_Text"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldTitle::get_Text 方法。获取或设置标题的文本（C++）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fieldtitle/get_text/
---
## FieldTitle::get_Text method


获取或设置标题的文本。

```cpp
System::String Aspose::Words::Fields::FieldTitle::get_Text()
```


## 示例



展示如何使用 TITLE 字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 为内置文档属性 "Title" 设置值。
doc->get_BuiltInDocumentProperties()->set_Title(u"My Title");

// 我们可以使用 TITLE 字段在文档中显示此属性的值。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldTitle>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, false));
field->Update();

ASSERT_EQ(u" TITLE ", field->GetFieldCode());
ASSERT_EQ(u"My Title", field->get_Result());

// 为字段的 Text 属性设置值，
// 然后更新字段时，也会用新值覆盖相应的内置属性。
builder->Writeln();
field = System::ExplicitCast<Aspose::Words::Fields::FieldTitle>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, false));
field->set_Text(u"My New Title");
field->Update();

ASSERT_EQ(u" TITLE  \"My New Title\"", field->GetFieldCode());
ASSERT_EQ(u"My New Title", field->get_Result());
ASSERT_EQ(u"My New Title", doc->get_BuiltInDocumentProperties()->get_Title());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TITLE.docx");
```

## 另见

* Class [FieldTitle](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
