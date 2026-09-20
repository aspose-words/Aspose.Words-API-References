---
title: "Aspose::Words::Fields::FieldDocVariable::get_VariableName 方法"
linktitle: "get_VariableName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldDocVariable::get_VariableName 方法。获取或设置在 C++ 中要检索的文档变量的名称。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fielddocvariable/get_variablename/
---
## FieldDocVariable::get_VariableName method


获取或设置要检索的文档变量的名称。

```cpp
System::String Aspose::Words::Fields::FieldDocVariable::get_VariableName()
```


## 示例



展示如何使用 DOCPROPERTY 字段显示文档属性和变量。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 以下是使用 DOCPROPERTY 字段的两种方法。
// 1 -  显示内置属性：
// 为内置属性 "Category" 设置自定义值，然后插入引用该属性的 DOCPROPERTY 字段。
doc->get_BuiltInDocumentProperties()->set_Category(u"My category");

auto fieldDocProperty = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY Category "));
fieldDocProperty->Update();

ASSERT_EQ(u" DOCPROPERTY Category ", fieldDocProperty->GetFieldCode());
ASSERT_EQ(u"My category", fieldDocProperty->get_Result());

builder->InsertParagraph();

// 2 -  显示自定义文档变量：
// 定义自定义变量，然后使用 DOCPROPERTY 字段引用该变量。
ASSERT_EQ(0, doc->get_Variables()->get_Count());
doc->get_Variables()->Add(u"My variable", u"My variable's value");

auto fieldDocVariable = System::ExplicitCast<Aspose::Words::Fields::FieldDocVariable>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDocVariable, true));
fieldDocVariable->set_VariableName(u"My Variable");
fieldDocVariable->Update();

ASSERT_EQ(u" DOCVARIABLE  \"My Variable\"", fieldDocVariable->GetFieldCode());
ASSERT_EQ(u"My variable's value", fieldDocVariable->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.DOCPROPERTY.DOCVARIABLE.docx");
```

## 另见

* Class [FieldDocVariable](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
