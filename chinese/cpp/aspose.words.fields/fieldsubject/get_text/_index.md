---
title: "Aspose::Words::Fields::FieldSubject::get_Text 方法"
linktitle: "get_Text"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldSubject::get_Text 方法。获取或设置 C++ 中主题的文本。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fieldsubject/get_text/
---
## FieldSubject::get_Text method


获取或设置主题的文本。

```cpp
System::String Aspose::Words::Fields::FieldSubject::get_Text()
```


## 示例



展示如何使用 SUBJECT 字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 为文档的 \"Subject\" 内置属性设置值。
doc->get_BuiltInDocumentProperties()->set_Subject(u"My subject");

// 创建一个 SUBJECT 字段以显示该内置属性的值。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSubject>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSubject, true));
field->Update();

ASSERT_EQ(u" SUBJECT ", field->GetFieldCode());
ASSERT_EQ(u"My subject", field->get_Result());

// 如果我们为 SUBJECT 字段的 Text 属性赋值并更新它，字段将
// 使用其 Text 属性的值覆盖 \"Subject\" 内置属性的当前值，
// 然后显示新值。
field->set_Text(u"My new subject");
field->Update();

ASSERT_EQ(u" SUBJECT  \"My new subject\"", field->GetFieldCode());
ASSERT_EQ(u"My new subject", field->get_Result());

ASSERT_EQ(u"My new subject", doc->get_BuiltInDocumentProperties()->get_Subject());

doc->Save(get_ArtifactsDir() + u"Field.SUBJECT.docx");
```

## 另见

* Class [FieldSubject](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
