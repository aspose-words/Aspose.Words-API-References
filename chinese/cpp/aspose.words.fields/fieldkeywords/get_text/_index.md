---
title: "Aspose::Words::Fields::FieldKeywords::get_Text 方法"
linktitle: "get_Text"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldKeywords::get_Text 方法。获取或设置关键字的文本（在 C++ 中）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fieldkeywords/get_text/
---
## FieldKeywords::get_Text method


获取或设置关键字的文本。

```cpp
System::String Aspose::Words::Fields::FieldKeywords::get_Text()
```


## 示例



展示如何插入 KEYWORDS 字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 添加一些关键字，在文件资源管理器中也称为 "标签"。
doc->get_BuiltInDocumentProperties()->set_Keywords(u"Keyword1, Keyword2");

// KEYWORDS 字段显示此属性的值。
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldKeywords>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldKeyword, true));
field->Update();

ASSERT_EQ(u" KEYWORDS ", field->GetFieldCode());
ASSERT_EQ(u"Keyword1, Keyword2", field->get_Result());

// 为字段的 Text 属性设置值，
// 然后更新字段时，也会用新值覆盖相应的内置属性。
field->set_Text(u"OverridingKeyword");
field->Update();

ASSERT_EQ(u" KEYWORDS  OverridingKeyword", field->GetFieldCode());
ASSERT_EQ(u"OverridingKeyword", field->get_Result());
ASSERT_EQ(u"OverridingKeyword", doc->get_BuiltInDocumentProperties()->get_Keywords());

doc->Save(get_ArtifactsDir() + u"Field.KEYWORDS.docx");
```

## 另见

* Class [FieldKeywords](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
