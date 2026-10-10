---
title: "Aspose::Words::Fields::FieldOptions::get_DefaultDocumentAuthor 方法"
linktitle: "get_DefaultDocumentAuthor"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldOptions::get_DefaultDocumentAuthor 方法。获取或设置默认文档作者的名称。如果作者名称已在内置文档属性中指定，则在 C++ 中不考虑此选项。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.fields/fieldoptions/get_defaultdocumentauthor/
---
## FieldOptions::get_DefaultDocumentAuthor method


获取或设置默认文档作者姓名。如果作者姓名已在内置文档属性中指定，则此选项不予考虑。

```cpp
System::String Aspose::Words::Fields::FieldOptions::get_DefaultDocumentAuthor() const
```


## 示例



展示如何使用 AUTHOR 字段来显示文档创建者的名称。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// AUTHOR 字段的结果来源于名为 "Author" 的内置文档属性。
// 如果我们在 Microsoft Word 中创建并保存文档，
// 该属性中将会包含我们的用户名。
// 但是，如果我们使用 Aspose.Words 以编程方式创建文档，
// 默认情况下，"Author" 属性将是空字符串。
ASSERT_EQ(System::String::Empty, doc->get_BuiltInDocumentProperties()->get_Author());

// 为 AUTHOR 字段设置备用作者名称
// 如果 "Author" 属性为空字符串。
doc->get_FieldOptions()->set_DefaultDocumentAuthor(u"Joe Bloggs");

builder->Write(u"This document was created by ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));
field->Update();

ASSERT_EQ(u" AUTHOR ", field->GetFieldCode());
ASSERT_EQ(u"Joe Bloggs", field->get_Result());

// 更新包含值的 AUTHOR 字段
// 将把该值应用到 "Author" 内置属性。
ASSERT_EQ(u"Joe Bloggs", doc->get_BuiltInDocumentProperties()->get_Author());

// 更改此属性后，再更新 AUTHOR 字段将把该值应用到字段中。
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
field->Update();

ASSERT_EQ(u" AUTHOR ", field->GetFieldCode());
ASSERT_EQ(u"John Doe", field->get_Result());

// 如果我们在更改其 "Name" 属性后更新 AUTHOR 字段，
// 则字段将显示新名称并将新名称应用到内置属性。
field->set_AuthorName(u"Jane Doe");
field->Update();

ASSERT_EQ(u" AUTHOR  \"Jane Doe\"", field->GetFieldCode());
ASSERT_EQ(u"Jane Doe", field->get_Result());

// AUTHOR 字段不会影响 DefaultDocumentAuthor 属性。
ASSERT_EQ(u"Jane Doe", doc->get_BuiltInDocumentProperties()->get_Author());
ASSERT_EQ(u"Joe Bloggs", doc->get_FieldOptions()->get_DefaultDocumentAuthor());

doc->Save(get_ArtifactsDir() + u"Field.AUTHOR.docx");
```

## 另见

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
