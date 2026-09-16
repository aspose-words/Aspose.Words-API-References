---
title: "Aspose::Words::Fields::FieldBuilder::FieldBuilder 构造函数"
linktitle: "FieldBuilder"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldBuilder::FieldBuilder 构造函数。 在 C++ 中初始化 FieldBuilder 类的实例。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fieldbuilder/fieldbuilder/
---
## FieldBuilder::FieldBuilder constructor


初始化 [FieldBuilder](../) 类的实例。

```cpp
Aspose::Words::Fields::FieldBuilder::FieldBuilder(Aspose::Words::Fields::FieldType fieldType)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | 要构建的字段的类型。 |

## 示例



展示如何使用字段构建器创建并插入字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 向文档添加文本内容的便捷方式是使用文档构建器。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u" Hello world! This text is one Run, which is an inline node.");

// 字段有各自的构建器，我们可以用它逐步构建字段代码。
// 在本例中，我们将构建一个表示美国邮政编码的 BARCODE 字段，
// 然后将其插入到 Run 前面。
auto fieldBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldBarcode);
fieldBuilder->AddArgument(u"90210");
fieldBuilder->AddSwitch(u"\\f", u"A");
fieldBuilder->AddSwitch(u"\\u");

fieldBuilder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.CreateWithFieldBuilder.docx");
```

## 另见

* Enum [FieldType](../../fieldtype/)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
