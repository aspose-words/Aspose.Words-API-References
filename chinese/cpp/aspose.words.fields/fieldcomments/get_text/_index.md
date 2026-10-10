---
title: "Aspose::Words::Fields::FieldComments::get_Text 方法"
linktitle: "get_Text"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldComments::get_Text 方法。获取或设置 C++ 中注释的文本。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fieldcomments/get_text/
---
## FieldComments::get_Text method


获取或设置注释的文本。

```cpp
System::String Aspose::Words::Fields::FieldComments::get_Text()
```


## 示例



展示如何使用 COMMENTS 字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 为文档的内置属性 "Comments" 设置一个值。
doc->get_BuiltInDocumentProperties()->set_Comments(u"My comment.");

// 创建一个 COMMENTS 字段以显示该内置属性的值。
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldComments>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldComments, true));
field->Update();

ASSERT_EQ(u" COMMENTS ", field->GetFieldCode());
ASSERT_EQ(u"My comment.", field->get_Result());

// 如果我们为 COMMENTS 字段的 Text 属性赋值并更新它，字段将
// 用其 Text 属性的值覆盖 "Comments" 内置属性的当前值，
// 然后显示新值。
field->set_Text(u"My overriding comment.");
field->Update();

ASSERT_EQ(u" COMMENTS  \"My overriding comment.\"", field->GetFieldCode());
ASSERT_EQ(u"My overriding comment.", field->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.COMMENTS.docx");
```

## 另见

* Class [FieldComments](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
