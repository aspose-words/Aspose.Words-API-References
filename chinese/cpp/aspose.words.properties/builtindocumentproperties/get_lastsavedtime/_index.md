---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime 方法"
linktitle: "get_LastSavedTime"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime 方法。获取或设置上次保存的 UTC 时间，在 C++ 中。"
type: docs
weight: 17000
url: /zh/cpp/aspose.words.properties/builtindocumentproperties/get_lastsavedtime/
---
## BuiltInDocumentProperties::get_LastSavedTime method


获取或设置上次保存的时间（UTC）。

```cpp
System::DateTime Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime()
```

## 备注


对于源自 RTF 格式的文档，此属性返回上次保存操作的本地时间。

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


展示如何使用 SAVEDATE 字段显示使用 Microsoft Word 执行的文档最近一次保存操作的日期/时间。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was last saved:");

// 我们可以使用 SAVEDATE 字段在文档上显示上一次保存操作的日期和时间。
// 这些字段所指的保存操作是类似 Microsoft Word 的应用程序中的手动保存，
// 而不是文档的 Save 方法。
// 以下是三种不同的日历类型，SAVEDATE 字段可以根据这些类型显示日期/时间。
// 1 - 伊斯兰阴历：
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\h", field->GetFieldCode());

// 2 -  Umm al-Qura 日历：
builder->Write(u"\nAccording to the Umm al-Qura calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\u", field->GetFieldCode());

// 3 - 印度国家日历：
builder->Write(u"\nAccording to the Indian National calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\s", field->GetFieldCode());

// SAVEDATE 字段从内置属性 LastSavedTime 获取其日期/时间值。
// 文档的 Save 方法不会更新此值，但我们仍然可以手动更新它。
doc->get_BuiltInDocumentProperties()->set_LastSavedTime(System::DateTime::get_Now());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SAVEDATE.docx");
```

## 另见

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
