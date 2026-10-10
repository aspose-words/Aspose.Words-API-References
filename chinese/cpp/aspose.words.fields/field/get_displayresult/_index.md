---
title: "Aspose::Words::Fields::Field::get_DisplayResult 方法"
linktitle: "get_DisplayResult"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::Field::get_DisplayResult 方法。获取在 C++ 中表示显示字段结果的文本。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/field/get_displayresult/
---
## Field::get_DisplayResult method


获取表示显示字段结果的文本。

```cpp
System::String Aspose::Words::Fields::Field::get_DisplayResult()
```


## 示例



展示如何获取字段在文档中实际显示的文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"This document was written by ");
auto fieldAuthor = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));
fieldAuthor->set_AuthorName(u"John Doe");

// 我们可以使用 DisplayResult 属性来验证确切的文本
// 字段将在文档中其位置显示的文本。
ASSERT_EQ(System::String::Empty, fieldAuthor->get_DisplayResult());

// 字段不会实时维护准确的结果值。
// 为了确保我们的字段在任何时候都显示准确的结果，
// 例如在保存操作之前，我们需要手动更新它们。
fieldAuthor->Update();

ASSERT_EQ(u"John Doe", fieldAuthor->get_DisplayResult());

doc->Save(get_ArtifactsDir() + u"Field.DisplayResult.docx");
```

## 另见

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
