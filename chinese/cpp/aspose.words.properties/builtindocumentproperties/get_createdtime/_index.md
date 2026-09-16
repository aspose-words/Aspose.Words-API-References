---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_CreatedTime method"
linktitle: "get_CreatedTime"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_CreatedTime method. 获取或设置文档创建的 UTC 日期，使用 C++。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words.properties/builtindocumentproperties/get_createdtime/
---
## BuiltInDocumentProperties::get_CreatedTime method


获取或设置文档创建日期（UTC）。

```cpp
System::DateTime Aspose::Words::Properties::BuiltInDocumentProperties::get_CreatedTime()
```

## 备注


对于源自 RTF 格式的文档，此属性返回作者机器在文档创建时的本地时间。

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

## 另见

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
