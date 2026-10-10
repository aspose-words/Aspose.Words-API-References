---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_RevisionNumber 方法"
linktitle: "get_RevisionNumber"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_RevisionNumber 方法。获取或设置文档的修订号（C++）。"
type: docs
weight: 24000
url: /zh/cpp/aspose.words.properties/builtindocumentproperties/get_revisionnumber/
---
## BuiltInDocumentProperties::get_RevisionNumber method


获取或设置文档修订号。

```cpp
int32_t Aspose::Words::Properties::BuiltInDocumentProperties::get_RevisionNumber()
```

## 备注


Aspose.Words 不会更新此属性。

## 示例



展示如何在 \"Origin\" 类别中使用文档属性。
```cpp
// 打开一个我们使用 Microsoft Word 创建和编辑的文档。
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

// 以下内置属性包含有关此文档创建和编辑的信息。
// 我们可以在 Windows Explorer 中右键单击此文档并找到
// 通过 \"Properties\" -> \"Details\" -> \"Origin\" 类别查看这些属性。
// 诸如 PRINTDATE 和 EDITTIME 等字段可以在文档正文中显示这些值。
std::cout << System::String::Format(u"Created using {0}, on {1}", properties->get_NameOfApplication(), properties->get_CreatedTime()) << std::endl;
std::cout << System::String::Format(u"Minutes spent editing: {0}", properties->get_TotalEditingTime()) << std::endl;
std::cout << System::String::Format(u"Date/time last printed: {0}", properties->get_LastPrinted()) << std::endl;
std::cout << System::String::Format(u"Template document: {0}", properties->get_Template()) << std::endl;

// 我们也可以更改内置属性的值。
properties->set_Company(u"Doe Ltd.");
properties->set_Manager(u"Jane Doe");
properties->set_Version(5);
System::WithLambda::setter_post_increment_wrap(GETTER_SETTER_LAMBDA_ARGS(properties, RevisionNumber));

// 当我们保存文档时，Microsoft Word 会自动更新以下属性。
// 要在 Aspose.Words 中使用这些属性，需要手动为它们设置值。
properties->set_LastSavedBy(u"John Doe");
properties->set_LastSavedTime(System::DateTime::get_Now());

// 我们可以在 Windows Explorer 中右键单击此文档，并在 \"Properties\" -> \"Details\" -> \"Origin\" 中找到这些属性。
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Origin.docx");
```


展示如何使用 REVNUM 字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Current revision #");

// 插入 REVNUM 字段，该字段显示文档的当前修订号属性。
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldRevNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRevisionNum, true));

ASSERT_EQ(u" REVNUM ", field->GetFieldCode());
ASSERT_EQ(u"1", field->get_Result());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_RevisionNumber());

// 此属性统计文档在 Microsoft Word 中被保存的次数，
// 且与已跟踪的修订无关。我们可以通过在 Windows 资源管理器中右键单击文档来找到它
// 通过属性 -> 详细信息。我们可以手动更新此属性。
System::WithLambda::setter_post_increment_wrap(GETTER_SETTER_LVAL_LAMBDA_ARGS(doc->get_BuiltInDocumentProperties(), RevisionNumber));
field->Update();

ASSERT_EQ(u"2", field->get_Result());
```

## 另见

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
