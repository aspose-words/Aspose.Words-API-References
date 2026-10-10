---
title: "Aspose::Words::Fields::FieldInfo::get_InfoType 方法"
linktitle: "get_InfoType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldInfo::get_InfoType 方法。获取或设置要在 C++ 中插入的文档属性的类型。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fieldinfo/get_infotype/
---
## FieldInfo::get_InfoType method


获取或设置要插入的文档属性的类型。

```cpp
System::String Aspose::Words::Fields::FieldInfo::get_InfoType()
```


## 示例



展示如何使用 INFO 字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 为内置属性 "Comments" 设置值，然后插入 INFO 字段以显示该属性的值。
doc->get_BuiltInDocumentProperties()->set_Comments(u"My comment");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldInfo>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInfo, true));
field->set_InfoType(u"Comments");
field->Update();

ASSERT_EQ(u" INFO  Comments", field->GetFieldCode());
ASSERT_EQ(u"My comment", field->get_Result());

builder->Writeln();

// 为字段的 NewValue 属性设置值并更新
// 该字段还会用新值覆盖相应的内置属性。
field = System::ExplicitCast<Aspose::Words::Fields::FieldInfo>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInfo, true));
field->set_InfoType(u"Comments");
field->set_NewValue(u"New comment");
field->Update();

ASSERT_EQ(u" INFO  Comments \"New comment\"", field->GetFieldCode());
ASSERT_EQ(u"New comment", field->get_Result());
ASSERT_EQ(u"New comment", doc->get_BuiltInDocumentProperties()->get_Comments());

doc->Save(get_ArtifactsDir() + u"Field.INFO.docx");
```

## 另见

* Class [FieldInfo](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
